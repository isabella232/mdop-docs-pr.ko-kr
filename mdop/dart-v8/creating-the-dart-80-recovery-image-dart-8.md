---
title: DaRT 8.0 복구 이미지 만들기
description: DaRT 8.0 복구 이미지 만들기
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812553"
---
# <span data-ttu-id="ca285-103">DaRT 8.0 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="ca285-103">Creating the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="ca285-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0을 설치한 후 DaRT 8.0 복구 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you create a DaRT 8.0 recovery image.</span></span> <span data-ttu-id="ca285-105">복구 이미지는 Windows RE를 시작 하 여 DaRT 도구를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="ca285-106">ISO (국제 표준화 기구) 파일과 WIM (Windows Imaging 형식) 이미지를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="ca285-107">또한 PowerShell을 사용 하 여 DaRT 복구 이미지 마법사에서 선택한 설정을 사용 하는 스크립트를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="ca285-108">나중에이 스크립트를 사용 하 여 동일한 설정을 사용 하 여 복구 이미지를 다시 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="ca285-109">복구 이미지는 다양 한 복구 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="ca285-110">도구에 대 한 설명은 [DaRT 8.0의 도구 개요](overview-of-the-tools-in-dart-80-dart-8.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-110">For a description of the tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

<span data-ttu-id="ca285-111">컴퓨터를 DaRT로 부팅 한 후 다른 DaRT 도구를 실행 하 여 컴퓨터를 진단 하 고 복구 해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="ca285-112">이 섹션에서는 DaRT 복구 이미지를 만드는 과정을 안내 하 고 이미지의 일부로 포함 하려는 도구와 기능을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="ca285-113">다음 두 가지 방법 중 하나를 사용 하 여 DaRT 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="ca285-114">Windows 환경에서 실행 되는 DaRT 복구 이미지 마법사를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="ca285-115">원하는 값을 사용 하 여 예제 PowerShell 스크립트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="ca285-116">자세한 내용은 [PowerShell 스크립트를 사용 하 여 복구 이미지를 만드는 방법을](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="ca285-117">기록 가능한 CD 또는 DVD에 ISO를 작성 하 고, USB 플래시 드라이브에 저장 하거나, 원격 파티션이나 복구 파티션에서 DaRT로 부팅 하는 데 사용할 수 있는 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="ca285-118">ISO 이미지를 만들었으면 빈 CD 또는 DVD (컴퓨터에 CD 또는 DVD 드라이브가 있는 경우)로 구울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="ca285-119">컴퓨터에이 용도의 드라이브가 없는 경우 Cd 또는 Dvd를 굽는 데 사용 되는 대부분의 일반적인 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="ca285-120">이미지 아키텍처를 선택 하 고 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="ca285-121">Windows 8 미디어 페이지에서 32 비트 또는 64 비트 DaRT 복구 이미지를 만들지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-121">On the Windows 8 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="ca285-122">32 비트 Windows를 사용 하 여 32 비트 DaRT 복구 이미지 및 64 비트 Windows를 작성 하 여 64 비트 DaRT 복구 이미지를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="ca285-123">단일 컴퓨터를 사용 하 여 두 아키텍처 유형 모두에 대 한 복구 이미지를 만들 수 있지만, 32 비트 및 64 비트 아키텍처 모두에서 작동 하는 하나의 이미지를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="ca285-124">또한 Windows 8 설치 미디어의 경로도 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-124">You also indicate the path of the Windows 8 installation media.</span></span> <span data-ttu-id="ca285-125">만들고 있는 복구 이미지 중 하 나와 일치 하는 아키텍처를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="ca285-126">이미지 아키텍처를 선택 하 고 경로를 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="ca285-127">**Windows 8 미디어** 페이지에서 다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-127">On the **Windows 8 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="ca285-128">64 비트 컴퓨터에 대 한 복구 이미지를 만드는 경우 **x64 (64 비트) DaRT 이미지 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="ca285-129">32 비트 컴퓨터에 대 한 복구 이미지를 만드는 경우 **x86 (32 비트) DaRT 이미지 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="ca285-130">**Windows 8 &lt; 64 비트 또는 32 비트 &gt; 설치 미디어의 루트 경로 지정** 상자에 windows 8 설치 파일의 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-130">In the **Specify the root path of the Windows 8 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 8 installation files.</span></span> <span data-ttu-id="ca285-131">만들고 있는 복구 이미지의 아키텍처와 일치 하는 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="ca285-132">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-132">Click **Next**.</span></span>

## <span data-ttu-id="ca285-133">복구 이미지에 포함할 도구 선택</span><span class="sxs-lookup"><span data-stu-id="ca285-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="ca285-134">도구 페이지에서 복구 이미지에 포함할 여러 도구를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="ca285-135">이러한 도구는 최종 사용자가 DaRT 이미지로 부팅 하는 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="ca285-136">그러나 DaRT 이미지를 만들 때 원격 연결을 사용 하도록 설정 하면 이미지에 포함 하도록 선택한 도구에 관계 없이 지원 센터 작업자에 게 최종 사용자의 컴퓨터에 연결 하는 경우 모든 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="ca285-137">이러한 도구에 대 한 최종 사용자의 액세스를 제한 하지만 원격 연결 뷰어를 통해 도구에 대 한 전체 액세스는 유지 하려면 도구 페이지에서 해당 도구를 선택 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="ca285-138">최종 사용자는 원격 연결만을 사용할 수 있으며, 복구 이미지에서 제외 된 도구는 볼 수만 있고 액세스는 하지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="ca285-139">복구 이미지에 포함할 도구를 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="ca285-140">**도구** 페이지에서 이미지에 포함 하려는 각 도구 옆에 있는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="ca285-141">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-141">Click **Next**.</span></span>

## <span data-ttu-id="ca285-142">헬프 데스크에의 한 원격 연결 허용 여부 선택</span><span class="sxs-lookup"><span data-stu-id="ca285-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="ca285-143">원격 연결 페이지에서 지원 센터 작업자에 게 원격으로 연결 하 여 최종 사용자의 컴퓨터에 있는 DaRT 도구를 실행할 수 있도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="ca285-144">그러면 원격 연결 옵션이 진단 및 복구 도구 집합 창에서 사용할 수 있는 옵션으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="ca285-145">지원 센터 작업자는 원격 연결을 설정 하 고 나면 원격 위치에서 최종 사용자 컴퓨터에 있는 DaRT 도구를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="ca285-146">지원 센터 근로자에의 한 원격 연결을 허용할지 여부를 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="ca285-147">**원격 연결** 페이지에서 원격 연결 **허용** 확인란을 선택 하 여 원격 연결을 허용 하거나 확인란의 선택을 취소 하 여 원격 연결을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="ca285-148">**원격 연결 허용** 확인란의 선택을 취소 한 경우 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="ca285-149">그렇지 않으면 다음 단계로 이동 하 여 원격 연결 구성을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="ca285-150">다음 중 하나를 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-150">Select one of the following:</span></span>

    -   <span data-ttu-id="ca285-151">Windows에서 열려 있는 포트 번호를 선택 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="ca285-152">포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-152">Specify the port number.</span></span> <span data-ttu-id="ca285-153">이 옵션을 선택 하는 경우 옵션 아래에 있는 필드에 1과 65535 사이의 포트 번호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="ca285-154">이 포트 번호는 원격 연결을 설정할 때 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="ca285-155">충돌의 가능성을 최소화 하기 위해 포트 번호를 1024 이상으로 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="ca285-156">(선택 사항) **원격 연결 시작** 메시지 상자에서 원격 연결을 설정할 때 최종 사용자가 받는 사용자 지정 메시지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="ca285-157">메시지는 최대 2048 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="ca285-158">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-158">Click **Next**.</span></span>

    <span data-ttu-id="ca285-159">DaRT 도구를 원격으로 실행 하는 방법에 대 한 자세한 내용은 [Dart 복구 이미지를 사용 하 여 원격 컴퓨터를 복구 하는 방법을](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

## <span data-ttu-id="ca285-160">복구 이미지에 드라이버 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="ca285-161">고급 옵션 페이지의 드라이버 탭에서 컴퓨터를 복구 하는 데 필요할 수 있는 추가 장치 드라이버를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="ca285-162">여기에는 일반적으로 Windows 8에서 제공 하지 않는 저장소 또는 네트워크 컨트롤러가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-162">These may typically include storage or network controllers that Windows 8 does not provide.</span></span> <span data-ttu-id="ca285-163">드라이버는 이미지를 만들 때 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="ca285-164">**중요**  포함할 드라이버를 선택할 때 무선 연결이 DaRT에서 지원 되지 않는다는 점에 유의 하세요 (예: Bluetooth 또는 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="ca285-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="ca285-165">복구 이미지에 드라이버 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="ca285-166">**고급 옵션** 페이지에서 **드라이버** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="ca285-167">**추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-167">Click **Add**.</span></span>

3.  <span data-ttu-id="ca285-168">드라이버에 추가할 파일을 찾은 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="ca285-169">**참고**  드라이버 파일은 저장소 또는 네트워크 컨트롤러의 제조업체에서 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="ca285-170">포함 하려는 모든 드라이버에 대해 2 ~ 3 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="ca285-171">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-171">Click **Next**.</span></span>

## <span data-ttu-id="ca285-172">복구 이미지에 WinPE 선택적 패키지 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="ca285-173">고급 옵션 페이지의 WinPE 탭에서 DaRT 이미지에 WinPE 선택적 패키지를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="ca285-174">이러한 패키지는 DaRT 복구 이미지 마법사의 설치 조건인 Windows ADK의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="ca285-175">선택할 수 있는 도구는 모두 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="ca285-176">필요한 패키지는 도구 페이지에서 선택한 도구에 따라 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="ca285-177">스크래치 공간 크기를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="ca285-178">스크래치 공간은 DaRT를 실행할 수 있도록 별도로 설정 된 RAM 디스크 공간 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="ca285-179">스크래치 공간은 최종 사용자의 하드 디스크를 사용할 수 없는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="ca285-180">추가 도구 및 드라이버를 실행 하는 경우 스크래치 공간을 늘려야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="ca285-181">복구 이미지에 WinPE 선택적 패키지 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="ca285-182">**고급 옵션** 페이지에서 **WinPE** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="ca285-183">각 패키지 옆에 있는 확인란을 선택 하 여 이미지에 포함 하거나, **이름** 확인란을 클릭 하 여 모든 패키지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="ca285-184">**스크래치 공간** 필드에서 최종 사용자의 하드 디스크를 사용할 수 없는 경우에는 DaRT를 실행 하기 위해 할당할 RAM 디스크 공간 크기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="ca285-185">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-185">Click **Next**.</span></span>

## <span data-ttu-id="ca285-186">충돌 분석기의 디버깅 도구 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="ca285-187">ISO 이미지에 충돌 분석기 도구를 포함 하는 경우 Windows 용 디버깅 도구도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="ca285-188">고급 옵션 페이지의 충돌 분석기 탭에서 충돌 분석기가 메모리 덤프 파일을 분석 하는 데 사용 하는 Windows 8 디버깅 도구 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 8 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="ca285-189">DaRT 복구 이미지 마법사를 실행 중인 컴퓨터에 있는 도구를 사용 하거나 최종 사용자 컴퓨터에 있는 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="ca285-190">최종 사용자 컴퓨터에서 도구를 사용 하기로 결정 한 경우, 진단 하는 모든 컴퓨터에 디버깅 도구가 설치 되어 있어야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="ca285-191">Microsoft Windows SDK (소프트웨어 개발 키트) 또는 WDK (Microsoft Windows 개발 키트)를 설치한 경우 Windows 8 디버깅 도구가 기본적으로 복구 이미지에 추가 되 고 디버깅 도구의 경로는 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 8 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="ca285-192">파일이 기본 파일 경로에 지정 된 위치가 아닌 다른 위치에 있는 경우 Windows 8 디버깅 도구의 경로를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-192">You can change the path of the Windows 8 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="ca285-193">마법사의 링크를 통해 Windows 용 디버깅 도구가 아직 설치 되어 있지 않은 경우이를 다운로드 하 여 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="ca285-194">Windows 디버깅 도구를 다운로드 하려면 [windows 용 디버깅 도구](https://go.microsoft.com/fwlink/?LinkId=266248)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca285-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="ca285-195">기본 위치에 디버깅 도구를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="ca285-196">**참고**  DaRT 마법사는 레지스트리 키의 도구를 확인 `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="ca285-197">레지스트리 값이 없는 경우 마법사는 시스템 아키텍처에 따라 다음 위치 중 하나를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**<span data-ttu-id="ca285-198">충돌 분석기에 대 한 디버깅 도구를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="ca285-199">**고급 옵션** 페이지에서 **충돌 분석기** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="ca285-200">) **디버깅 도구 다운로드** 를 클릭 하 여 Windows 용 디버깅 도구를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="ca285-201">다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="ca285-202">**Windows 8 &lt; 64 비트 또는 32 비트 &gt; 디버깅 도구를 포함**합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-202">**Include the Windows 8 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="ca285-203">이 옵션을 선택 하는 경우 경로가 아직 표시 되지 않은 경우 도구 위치를 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="ca285-204">**디버그 중인 시스템의 디버깅 도구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="ca285-205">이 옵션을 선택 하면 Windows 용 디버깅 도구가 문제 컴퓨터에 없는 경우 충돌 분석기가 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="ca285-206">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-206">Click **Next**.</span></span>

## <span data-ttu-id="ca285-207">Defender 도구에 대 한 정의 추가</span><span class="sxs-lookup"><span data-stu-id="ca285-207">Add definitions for the Defender tool</span></span>


<span data-ttu-id="ca285-208">고급 옵션 페이지의 Defender 탭에서 Defender 도구에서 사용 하는 정의를 추가 하 여 컴퓨터에서 설치, 실행 또는 변경 하려는 소프트웨어가 원하지 않거나 악의적인 소프트웨어 인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-208">On the Defender tab of the Advanced Options page, you add definitions, which are used by the Defender tool to determine whether software that is trying to install, run, or change settings on a computer is unwanted or malicious software.</span></span>

**<span data-ttu-id="ca285-209">Defender 도구에 대 한 정의를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-209">To add definitions for the Defender tool</span></span>**

1.  <span data-ttu-id="ca285-210">**고급 옵션** 페이지에서 **Defender** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-210">On the **Advanced Options** page, click the **Defender** tab.</span></span>

2.  <span data-ttu-id="ca285-211">다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-211">Select one of the following options:</span></span>

    -   <span data-ttu-id="ca285-212">**최신 정의 다운로드 (권장)** – 정의 업데이트가 자동으로 시작 되 고 정의가 DaRT 복구 이미지에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-212">**Download the latest definitions (Recommended)** – The definition update starts automatically, and the definitions are added to the DaRT recovery image.</span></span> <span data-ttu-id="ca285-213">이 옵션은 정의를 사용할 수 없는 경우를 방지 하는 데 도움이 되는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-213">This option is recommended to help you avoid cases where the definitions might not be available.</span></span> <span data-ttu-id="ca285-214">정의를 다운로드 하려면 인터넷에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-214">You must be connected to the Internet to download the definitions.</span></span>

    -   <span data-ttu-id="ca285-215">**나중에 정의 다운로드** – 정의가 dart 복구 이미지에 포함 되지 않으며, dart를 실행 하는 컴퓨터에서 정의를 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-215">**Download the definitions later** – Definitions will not be included in the DaRT recovery image, and you will need to download the definitions from the computer that is running DaRT.</span></span>

        <span data-ttu-id="ca285-216">복구 이미지에 최신 정의를 포함 하지 않으려는 경우 또는 복구 이미지에 포함 된 정의가 더 이상 현재 Defender를 사용할 준비가 되어 있지 않은 경우에는 Defender에서 제공 하는 지침에 따라 검색을 시작 하기 전에 최신 정의를 구하십시오.</span><span class="sxs-lookup"><span data-stu-id="ca285-216">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use Defender, obtain the latest definitions before you begin a scan by following the instructions that are provided in Defender.</span></span>

        <span data-ttu-id="ca285-217">**중요**  정의가 없는 경우 스캔할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-217">**Important** You cannot scan if there are no definitions.</span></span>

         

3.  <span data-ttu-id="ca285-218">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-218">Click **Next**.</span></span>

## <span data-ttu-id="ca285-219">만들 복구 이미지 파일 형식 선택</span><span class="sxs-lookup"><span data-stu-id="ca285-219">Select the types of recovery image files to create</span></span>


<span data-ttu-id="ca285-220">이미지 만들기 페이지에서 복구 이미지에 대 한 출력 폴더를 선택 하 고, 이미지 이름을 입력 하 고, 만들 DaRT 복구 이미지 파일의 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-220">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="ca285-221">복구 이미지 만들기 프로세스가 진행 되는 동안 Windows 원본 파일의 압축을 풀고, DaRT 파일이이 폴더에 복사 되 고,이 페이지에서 선택한 파일 형식으로 이미지가 "다시 압축" 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-221">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="ca285-222">사용할 수 있는 이미지 파일 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-222">The available image file types are:</span></span>

-   <span data-ttu-id="ca285-223">**WIM (Windows Imaging 파일)** -PXE (부팅 실행 환경) 또는 로컬 파티션에 DaRT를 배포 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-223">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="ca285-224">**ISO 이미지 파일** -CD 또는 DVD에 배포 하거나 VM (가상 컴퓨터)에서 사용 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-224">**ISO image file** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="ca285-225">CD 또는 DVD를 굽는 대부분의 프로그램에는 해당 확장이 필요 하기 때문에 마법사에서 ISO 이미지에는 .iso 확장명을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-225">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="ca285-226">다른 위치를 지정 하지 않으면 이름 DaRT8와 함께 바탕 화면에 ISO 이미지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-226">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT8.ISO.</span></span>

-   <span data-ttu-id="ca285-227">**PowerShell 스크립트** – Dart 복구 이미지 마법사를 사용 하 여 선택할 수 있는 옵션을 기본적으로 제공 하는 명령으로 dart 복구 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-227">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="ca285-228">또한이 스크립트를 사용 하 여 DaRT 복구 이미지에서 파일을 추가 하거나 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-228">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="ca285-229">이 페이지에서 이미지 편집 확인란을 선택 하면 이미지 만들기 프로세스 중에 복구 이미지를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-229">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="ca285-230">예를 들어 "winpeshl.ini" 파일을 변경 하 여 사용자 지정 시작 순서를 만들거나 타사 도구를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-230">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="ca285-231">만들 복구 이미지 파일의 형식을 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-231">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="ca285-232">**이미지 만들기** 페이지에서 **찾아보기를** 클릭 하 여 이미지 파일의 출력 폴더를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-232">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="ca285-233">**참고**  이미지 크기는 사용자가 선택 하는 도구와 마법사에서 추가 하는 파일에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-233">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="ca285-234">**이미지 이름** 상자에 DaRT 복구 이미지의 이름을 입력 하거나 기본 이름 (DaRT8)을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-234">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT8.</span></span>

    <span data-ttu-id="ca285-235">마법사에서이 이름으로 출력 경로에 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-235">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="ca285-236">만들려는 이미지 파일 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-236">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="ca285-237">다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-237">Choose one of the following:</span></span>

    -   <span data-ttu-id="ca285-238">이미지 파일을 만들기 전에 복구 이미지의 파일을 변경 하려면 **이미지 편집** 확인란을 선택 하 고 **준비**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-238">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="ca285-239">파일을 변경 하지 않고 복구 이미지를 만들려면 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-239">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="ca285-240">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-240">Click **Next**.</span></span>

## <span data-ttu-id="ca285-241">복구 이미지 파일 편집</span><span class="sxs-lookup"><span data-stu-id="ca285-241">Edit the recovery image files</span></span>


<span data-ttu-id="ca285-242">이미지 만들기 페이지의 이미지 편집 확인란을 선택한 경우에만 복구 이미지를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-242">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="ca285-243">복구 이미지를 편집할 준비가 된 후에는 부팅 가능 미디어를 만들기 전에 복구 이미지 파일을 추가 하 고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-243">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="ca285-244">예를 들어 시작에 대 한 사용자 지정 순서를 만들고 다양 한 타사 도구를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-244">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="ca285-245">복구 이미지 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-245">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="ca285-246">**이미지 편집** 페이지에서 Windows 탐색기에서 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-246">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="ca285-247">대화 상자에 나열 된 폴더에 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-247">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="ca285-248">원하는 파일을 새 하위 폴더에 복사 하거나 필요 하지 않은 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-248">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="ca285-249">**만들기** 를 클릭 하 여 복구 이미지 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-249">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="ca285-250">복구 이미지 파일 생성</span><span class="sxs-lookup"><span data-stu-id="ca285-250">Generate the recovery image files</span></span>


<span data-ttu-id="ca285-251">파일 생성 페이지에서 이미지 만들기 페이지에서 선택한 파일 형식에 대 한 DaRT 복구 이미지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-251">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="ca285-252">복구 이미지 파일을 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-252">To generate the recovery image files</span></span>**

-   <span data-ttu-id="ca285-253">**파일 생성** 페이지에서 **다음** 을 클릭 하 여 복구 이미지 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-253">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="ca285-254">복구 이미지를 CD, DVD 또는 USB에 복사</span><span class="sxs-lookup"><span data-stu-id="ca285-254">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="ca285-255">부팅 가능 미디어 만들기 페이지에서 선택적으로 이미지 파일을 CD, DVD 또는 UFD (USB 플래시 드라이브)에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-255">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="ca285-256">마법사를 다시 시작 하 여이 페이지에서 부팅 가능한 미디어를 추가로 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-256">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="ca285-257">**참고**  PXE (부팅 전 실행 환경) 및 로컬 이미지 배포는 System Center Configuration Manager 서버 및 Microsoft 개발 도구 키트와 같은 추가 엔터프라이즈 도구를 필요로 하므로 기본적으로이 도구를 통해 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-257">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="ca285-258">복구 이미지를 CD, DVD 또는 USB에 복사 하려면</span><span class="sxs-lookup"><span data-stu-id="ca285-258">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="ca285-259">**부팅 가능 미디어 만들기** 페이지에서 복사 하려는 iso 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-259">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="ca285-260">CD, DVD 또는 USB를 삽입 한 다음 드라이브를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-260">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="ca285-261">**참고**  드라이브가 인식 되지 않고 새 드라이브를 설치 하는 경우 **새로 고침** 을 클릭 하 여 마법사에서 사용 가능한 드라이브 목록을 강제로 업데이트 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-261">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="ca285-262">**부팅 가능 미디어 만들기** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-262">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="ca285-263">다른 복구 이미지를 만들려면 다시 시작을 클릭 하거나 원하는 모든 미디어 만들기가 완료 되 면 **닫기를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca285-263">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="ca285-264">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ca285-264">Related topics</span></span>


[<span data-ttu-id="ca285-265">DaRT 8.0의 도구 개요</span><span class="sxs-lookup"><span data-stu-id="ca285-265">Overview of the Tools in DaRT 8.0</span></span>](overview-of-the-tools-in-dart-80-dart-8.md)

[<span data-ttu-id="ca285-266">DaRT 8.0 배포</span><span class="sxs-lookup"><span data-stu-id="ca285-266">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





