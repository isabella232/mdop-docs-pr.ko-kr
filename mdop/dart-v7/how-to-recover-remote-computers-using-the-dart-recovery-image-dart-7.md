---
title: DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822793"
---
# <span data-ttu-id="fa736-103">DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa736-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="fa736-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7의 원격 연결 기능을 사용 하면 IT 관리자가 최종 사용자 컴퓨터에서 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="fa736-105">최종 사용자가 특정 정보를 제공 하거나 (또는 사용자 컴퓨터에서 지원 되는 헬프데스크 전문가 인 경우) IT 관리자 또는 헬프데스크 에이전트는 최종 사용자의 컴퓨터를 제어 하 고 필요한 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="fa736-106">중요</span><span class="sxs-lookup"><span data-stu-id="fa736-106">Important</span></span>**  
<span data-ttu-id="fa736-107">원격 연결을 설정 하는 두 컴퓨터는 동일한 네트워크의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="fa736-108">DaRT를 사용 하 여 원격 컴퓨터를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="fa736-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="fa736-109">DaRT 복구 이미지를 사용 하 여 최종 사용자 컴퓨터를 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="fa736-110">일반적으로 dart 복구 이미지를 배포 하는 방법에 따라 다음 방법 중 하나를 사용 하 여 DaRT로 부팅 하 고 원격 컴퓨터를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="fa736-111">DaRT 복구 이미지 배포에 대 한 자세한 내용은 [dart 7.0 복구 이미지 배포](deploying-the-dart-70-recovery-image-dart-7.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa736-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="fa736-112">문제가 있는 컴퓨터의 복구 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="fa736-113">네트워크의 원격 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="fa736-114">각 방법의 장점과 단점에 대 한 자세한 내용은 [DaRT 7.0 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa736-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="fa736-115">DaRT로 부팅 하는 데 사용 하는 방법에 관계 없이 부팅 옵션에 대 한 부팅 장치를 사용 하도록 설정 하 고 최종 사용자가 사용할 수 있도록 할 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="fa736-116">참고</span><span class="sxs-lookup"><span data-stu-id="fa736-116">Note</span></span>**  
    <span data-ttu-id="fa736-117">BIOS 구성은 조직에 사용 되는 하드 디스크 드라이브, 네트워크 어댑터 및 기타 하드웨어의 종류에 따라 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="fa736-118">컴퓨터를 DaRT 복구 이미지로 부팅 하면 **Netstart** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="fa736-119">네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="fa736-120">**예**를 클릭 하면 DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="fa736-121">네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="fa736-122">네트워크 초기화 프로세스를 건너뛰려면 **아니요**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="fa736-123">네트워크 초기화 대화 상자를 팔 로우 하는 경우 드라이브 문자를 다시 매핑할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="fa736-124">Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="fa736-125">다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="fa736-126">나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="fa736-127">다시 매핑 대화 상자 다음에는 **시스템 복구 옵션** 대화 상자가 나타나고 키보드 레이아웃을 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="fa736-128">그러면 시스템 루트 디렉터리, 설치 된 운영 체제 종류 및 파티션 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="fa736-129">운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="fa736-130">장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="fa736-131">복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="fa736-132">참고</span><span class="sxs-lookup"><span data-stu-id="fa736-132">Note</span></span>**  
    <span data-ttu-id="fa736-133">WinRE (Windows 복구 환경)에서 Windows 7을 마지막으로 시도 했을 때 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구** 는 자동으로 실행 되기 시작 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="fa736-134">해결 방법을 비롯 한이 상황에 대 한 자세한 내용은 [DaRT 7.0 문제 해결](troubleshooting-dart-70-new-ia.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa736-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="fa736-135">**시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합** 을 선택 하 여 **진단 및 복구 도구 집합** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="fa736-136">**진단 및 복구 도구 집합** 창에서 **원격 연결** 을 클릭 하 여 **DaRT 원격 연결** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="fa736-137">지원 센터 원격 액세스를 제공 하 라는 메시지가 표시 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="fa736-138">DaRT 원격 연결 창이 열리고 티켓 번호, IP 주소 및 포트 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="fa736-139">헬프데스크 에이전트 컴퓨터에서 **DaRT 원격 연결 뷰어**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="fa736-140">**시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **Microsoft dart 7**을 클릭 한 다음 **DaRT 원격 연결 뷰어**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="fa736-141">**DaRT 원격 연결** 창에서 필요한 티켓, IP 주소 및 포트 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="fa736-142">참고</span><span class="sxs-lookup"><span data-stu-id="fa736-142">Note</span></span>**  
   <span data-ttu-id="fa736-143">이 정보는 최종 사용자 컴퓨터에서 생성 되며 최종 사용자가 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="fa736-144">최종 사용자 컴퓨터에서 사용할 수 있는 여러 개의 IP 주소를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="fa736-145">**연결**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-145">Click **Connect**.</span></span>

<span data-ttu-id="fa736-146">IT 관리자는 이제 최종 사용자 컴퓨터의 제어권을가지고 있으며 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="fa736-147">참고</span><span class="sxs-lookup"><span data-stu-id="fa736-147">Note</span></span>**  
<span data-ttu-id="fa736-148">inv32.xml 라는 이름의 파일이 제공 되며, 포트 번호 및 IP 주소와 같은 원격 연결 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="fa736-149">기본적으로 파일 은%windir%\\system32.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="fa736-150">원격 연결 프로세스를 사용자 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="fa736-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="fa736-151">winpeshl.ini 파일을 편집 하 여 원격 연결 프로세스를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="fa736-152">winpeshl.ini 파일을 편집 하는 방법에 대 한 자세한 내용은 [Winpeshl.ini 파일](https://go.microsoft.com/fwlink/?LinkId=219413)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa736-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="fa736-153">다음 명령과 매개 변수를 지정 하 여 최종 사용자 컴퓨터에서 원격 연결을 설정 하는 방법을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fa736-154">명령</span><span class="sxs-lookup"><span data-stu-id="fa736-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="fa736-155">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa736-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="fa736-156">설명</span><span class="sxs-lookup"><span data-stu-id="fa736-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="fa736-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="fa736-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="fa736-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="fa736-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fa736-159">확인 메시지가 표시 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="fa736-160">원격 연결은 </strong> 최종 사용자가 &quot; 확인 메시지에 Yes로 응답 한 것 처럼 계속 됩니다 &quot; .</span><span class="sxs-lookup"><span data-stu-id="fa736-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="fa736-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="fa736-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="fa736-162">none</span><span class="sxs-lookup"><span data-stu-id="fa736-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fa736-163"><strong>원격 연결이 실행 되 고 </strong> 있지 않거나 최종 사용자 컴퓨터에 유효한 연결이 설정 될 때까지 사용자 지정 스크립트가 계속 진행 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="fa736-164">중요</span><span class="sxs-lookup"><span data-stu-id="fa736-164">Important</span></span></strong><br/><p><span data-ttu-id="fa736-165">이 명령은 독립적으로 지정 된 경우 기능을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="fa736-166">올바르게 작동 하려면 스크립트에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="fa736-167">다음은 DaRT로 부팅 하려고 하는 즉시 **원격 연결** 도구를 열기 위해 사용자 지정 된 winpeshl.ini 파일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="fa736-168">명령 프롬프트에서 원격 연결 뷰어를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="fa736-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="fa736-169">명령 프롬프트에서 **DartRemoteViewer.exe** 명령을 지정 하 고 다음 매개 변수를 사용 하 여 **DaRT 원격 연결 뷰어** 를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fa736-170">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa736-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="fa736-171">설명</span><span class="sxs-lookup"><span data-stu-id="fa736-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa736-172">-ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="fa736-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa736-173">여기서 &lt; <em> ticketnumber </em> &gt; 는 대시를 포함 하 여 원격 연결에 의해 생성 되는 티켓 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa736-174">-ipaddress = &lt; <em> ipaddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="fa736-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa736-175">여기서 &lt; <em> Ipaddress </em> &gt; 는 원격 연결에 의해 생성 되는 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa736-176">-port = &lt; <em> port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="fa736-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa736-177">여기서 &lt; <em> 포트는 </em> &gt; 지정 된 IP 주소에 해당 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="fa736-178">세 개의 매개 변수가 모두 지정 되 고 데이터가 유효 하면 프로그램을 시작할 때 즉시 연결을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="fa736-179">매개 변수가 유효 하지 않은 경우에는 지정 된 매개 변수가 없는 것 처럼 프로그램이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa736-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="fa736-180">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fa736-180">Related topics</span></span>


[<span data-ttu-id="fa736-181">DaRT 7.0를 사용하여 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="fa736-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









