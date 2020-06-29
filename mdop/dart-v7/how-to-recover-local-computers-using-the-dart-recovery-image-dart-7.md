---
title: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823763"
---
# <span data-ttu-id="3cf8f-103">DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="3cf8f-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="3cf8f-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7을 사용 하 여 로컬 컴퓨터를 복구 하려면 DaRT가 필요한 문제가 발생 하는 최종 사용자 컴퓨터에 실제로 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="3cf8f-105">[Dart 복구 이미지를 사용 하 여 원격 컴퓨터를 복구 하는 방법](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)에 대 한 지침을 따라 원격으로 dart를 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="3cf8f-106">DaRT를 사용 하 여 로컬 컴퓨터를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="3cf8f-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="3cf8f-107">컴퓨터를 DaRT 복구 이미지로 부팅 하면 **Netstart** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="3cf8f-108">네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="3cf8f-109">**예**를 클릭 하면 DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="3cf8f-110">네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="3cf8f-111">네트워크 초기화 프로세스를 건너뛰려면 **아니요**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="3cf8f-112">네트워크 초기화 대화 상자를 팔 로우 하는 경우 드라이브 문자를 다시 매핑할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="3cf8f-113">Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="3cf8f-114">다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="3cf8f-115">나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="3cf8f-116">다시 매핑 대화 상자 다음에는 **시스템 복구 옵션** 대화 상자가 나타나고 키보드 레이아웃을 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="3cf8f-117">그러면 시스템 루트 디렉터리, 설치 된 운영 체제 종류 및 파티션 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="3cf8f-118">운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="3cf8f-119">장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="3cf8f-120">복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="3cf8f-121">참고</span><span class="sxs-lookup"><span data-stu-id="3cf8f-121">Note</span></span>**  
    <span data-ttu-id="3cf8f-122">WinRE (Windows 복구 환경)에서 Windows 7을 마지막으로 시도 했을 때 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구** 는 자동으로 실행 되기 시작 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="3cf8f-123">**시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="3cf8f-124">**진단 및 복구 도구 집합** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="3cf8f-125">이제 DaRT 복구 이미지를 만들 때 포함 된 개별 도구 또는 마법사를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="3cf8f-126">**진단 및 복구 도구 집합** 창에서 **도움말** 을 클릭 하 여 개별 DaRT 도구를 실행 하는 데 필요한 자세한 지침과 정보를 제공 하는 클라이언트 도움말 파일을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="3cf8f-127">**진단 및 복구 도구 집합** 창에서 **솔루션 마법사** 를 클릭 하 여 마법사가 제공 하는 간략 한 인터뷰에 따라 상황에 가장 적합 한 도구를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="3cf8f-128">DaRT 도구에 대 한 일반적인 정보는 [dart 7.0의 도구 개요](overview-of-the-tools-in-dart-70-new-ia.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="3cf8f-129">명령 프롬프트에서 DaRT를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="3cf8f-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="3cf8f-130">명령 프롬프트에서 **netstart.exe** 명령을 지정 하 고 다음 매개 변수를 사용 하 여 DaRT를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="3cf8f-131">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3cf8f-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="3cf8f-132">설명</span><span class="sxs-lookup"><span data-stu-id="3cf8f-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3cf8f-133">-네트워크</span><span class="sxs-lookup"><span data-stu-id="3cf8f-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3cf8f-134">네트워크 서비스를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3cf8f-135">-탑재</span><span class="sxs-lookup"><span data-stu-id="3cf8f-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3cf8f-136">드라이브 문자를 다시 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3cf8f-137">-프롬프트</span><span class="sxs-lookup"><span data-stu-id="3cf8f-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3cf8f-138">최종 사용자에 게 네트워크 초기화 및 드라이브 다시 매핑 여부를 지정 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="3cf8f-139">중요</span><span class="sxs-lookup"><span data-stu-id="3cf8f-139">Important</span></span></strong><br/><p><span data-ttu-id="3cf8f-140">메시지에 대 한 최종 사용자의 응답은-network 및-탑재 스위치를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="3cf8f-141">Dart로 부팅 하는 컴퓨터가 지원 센터와의 원격 연결을 설정 하는 데 사용 되는 **원격 연결** 도구를 자동으로 열려면 dart를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf8f-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="3cf8f-142">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3cf8f-142">Related topics</span></span>


[<span data-ttu-id="3cf8f-143">DaRT 7.0를 사용하여 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="3cf8f-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









