---
title: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822588"
---
# <span data-ttu-id="87027-103">DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="87027-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="87027-104">문제가 발생 하는 최종 사용자 컴퓨터에 컴퓨터를 설치 하는 경우 다음 지침을 사용 하 여 컴퓨터를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="87027-105">DaRT 복구 이미지를 사용 하 여 로컬 컴퓨터를 복구 하는 방법</span><span class="sxs-lookup"><span data-stu-id="87027-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="87027-106">Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지를 사용 하 여 최종 사용자 컴퓨터를 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

    <span data-ttu-id="87027-107">컴퓨터가 DaRT 10 복구 이미지로 부팅 될 때 **Netstart** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="87027-107">As the computer is booting into the DaRT 10 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="87027-108">네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 되 면 다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="87027-109">**Yes** -DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="87027-110">네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="87027-111">**No** -네트워크 초기화 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="87027-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="87027-112">드라이브 문자를 다시 매핑할 것인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87027-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="87027-113">Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="87027-114">다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="87027-115">나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87027-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="87027-116">**시스템 복구 옵션** 대화 상자에서 키보드 레이아웃을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="87027-117">표시 된 시스템 루트 디렉터리, 설치 된 운영 체제 종류, 파티션 크기를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="87027-118">운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 한 다음 장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="87027-119">복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="87027-120">참고</span><span class="sxs-lookup"><span data-stu-id="87027-120">Note</span></span>**  
    <span data-ttu-id="87027-121">Windows 10 복구 환경 (WinRE)에서 마지막으로 시도 했을 때 Windows 10이 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구가** 자동으로 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="87027-122">**시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="87027-123">**진단 및 복구 도구 집합** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="87027-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="87027-124">이제 DaRT 복구 이미지를 만들 때 포함 된 개별 도구 또는 마법사를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="87027-125">**진단 및 복구 도구 집합** 창에서 **도움말** 을 클릭 하 여 개별 DaRT 도구를 실행 하는 데 필요한 자세한 지침과 정보를 제공 하는 클라이언트 도움말 파일을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="87027-126">**진단 및 복구 도구 집합** 창에서 **솔루션 마법사** 를 클릭 하 여 마법사가 제공 하는 간략 한 인터뷰에 따라 상황에 가장 적합 한 도구를 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87027-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="87027-127">DaRT 도구에 대 한 일반적인 정보는 [dart 10의 도구 개요](overview-of-the-tools-in-dart-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="87027-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

**<span data-ttu-id="87027-128">명령 프롬프트에서 DaRT를 실행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="87027-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="87027-129">명령 프롬프트에서 DaRT를 실행 하려면 **netstart.exe** 명령을 지정 하 고 다음 매개 변수 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="87027-130">매개 변수</span><span class="sxs-lookup"><span data-stu-id="87027-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="87027-131">설명</span><span class="sxs-lookup"><span data-stu-id="87027-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="87027-132">-네트워크</span><span class="sxs-lookup"><span data-stu-id="87027-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="87027-133">네트워크 서비스를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="87027-134">-탑재</span><span class="sxs-lookup"><span data-stu-id="87027-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="87027-135">드라이브 문자를 다시 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="87027-136">-프롬프트</span><span class="sxs-lookup"><span data-stu-id="87027-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="87027-137">최종 사용자에 게 네트워크 초기화 및 드라이브 다시 매핑 여부를 지정 하도록 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="87027-138">Warning</span><span class="sxs-lookup"><span data-stu-id="87027-138">Warning</span></span></strong><br/><p><span data-ttu-id="87027-139">프롬프트에 대 한 최종 사용자의 응답은 – network 및 – 다시 탑재 스위치 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="87027-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="87027-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="87027-140">Related topics</span></span>


[<span data-ttu-id="87027-141">DaRT 10 작업</span><span class="sxs-lookup"><span data-stu-id="87027-141">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="87027-142">DaRT 10을 사용하여 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="87027-142">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









