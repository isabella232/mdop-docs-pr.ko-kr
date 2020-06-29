---
title: DaRT 복구 이미지 마법사를 사용하여 복구 이미지를 만드는 방법
description: DaRT 복구 이미지 마법사를 사용하여 복구 이미지를 만드는 방법
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822923"
---
# <span data-ttu-id="42caa-103">DaRT 복구 이미지 마법사를 사용하여 복구 이미지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="42caa-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="42caa-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7에는 Windows에서 부팅 가능한 국제 표준화 (ISO) 이미지를 만드는 데 사용 되는 **DaRT 복구 이미지 마법사** 가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="42caa-105">ISO 이미지는 CD의 원시 콘텐츠를 나타내는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="42caa-106">**DaRT 복구 이미지 마법사** 에는 다음 정보가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="42caa-107">**부팅 이미지**° DaRT 복구 이미지를 만드는 데 필요한 WINDOWS 7 DVD 또는 windows 7 원본 파일의 경로를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="42caa-108">**도구 선택**스타일 DaRT 복구 이미지에 포함할 도구를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="42caa-109">**원격 연결**°-DaRT 복구 이미지에 헬프데스크 및 최종 사용자 컴퓨터 간의 원격 연결을 설정 하는 기능을 포함할지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="42caa-110">**Windows 용 디버깅 도구**windows 용 디버깅 도구 위치를 제공 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="42caa-111">**독립 실행형 시스템 Sweeper에 대 한 정의**복구 이미지를 만들 때 최신 정의를 다운로드할지 여부를 결정 하거나 나중에 정의를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="42caa-112">**드라이버**를 통해 ISO 이미지에 드라이버를 추가할지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="42caa-113">**추가 파일**, 문제를 진단 하는 데 도움이 되는 파일을 ISO 이미지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="42caa-114">**Iso 이미지 위치**° ° iso 이미지를 배치할 위치를 지정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="42caa-115">Cd **/Dvd 드라이브**° ° cd 또는 dvd 드라이브를 사용 하 여 CD 또는 dvd를 굽는 지 여부를 지정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="42caa-116">**참고**  ISO 이미지 크기는 **DaRT 복구 이미지 마법사**에서 선택한 도구에 따라 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="42caa-117">DaRT 복구 이미지 마법사를 사용 하 여 복구 이미지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="42caa-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="42caa-118">**Dart 복구 이미지 마법사** 를 사용 하 여 dart 복구 이미지를 만들려면 다음 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="42caa-119">DaRT 복구 이미지에 포함할 도구를 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="42caa-120">**DaRT 복구 이미지 마법사** 는 **도구 선택** 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="42caa-121">도구를 강조 표시 한 다음 **사용** 또는 **사용 안 함** 단추를 클릭 하 여 DaRT 복구 이미지에 포함할 도구 목록에서 도구를 선택 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="42caa-122">복구 이미지에 포함 하려는 모든 도구를 선택 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="42caa-123">원격 연결을 허용 하는 옵션을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="42caa-124">**원격 연결 허용** 확인란을 선택 하 여 **진단 및 복구 도구 집합** 창에서 헬프데스크 에이전트와 최종 사용자 컴퓨터 간에 원격 연결을 설정 하는 옵션을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="42caa-125">헬프데스크 에이전트는 원격 연결을 설정 하 고 나면 원격 위치에서 최종 사용자 컴퓨터에 있는 DaRT 도구를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="42caa-126">**포트 번호 지정** 확인란을 선택 하 여 원격 연결을 설정할 때 사용 되는 특정 포트 번호를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="42caa-127">1에서 65535 사이의 포트 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="42caa-128">충돌의 가능성을 최소화 하기 위해 포트 번호를 1024 이상으로 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="42caa-129">원격 연결을 설정할 때 최종 사용자가 받는 사용자 지정 메시지를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="42caa-130">메시지는 최대 2048 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="42caa-131">DaRT 도구를 원격으로 실행 하는 방법에 대 한 자세한 내용은 [Dart 복구 이미지를 사용 하 여 원격 컴퓨터를 복구 하는 방법을](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="42caa-132">Windows 용 디버깅 도구를 DaRT 복구 이미지에 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="42caa-133">**DaRT 복구 이미지 마법사**의 **크래시 분석기** 대화 상자에서 Windows 용 디버깅 도구 위치를 지정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="42caa-134">도구의 복사본이 없는 경우 Microsoft에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="42caa-135">다운로드 페이지에 대 한 다음 링크는 마법사에 제공 됩니다. [Windows 용 디버깅 도구를 다운로드 하 고 설치](https://go.microsoft.com/fwlink/?LinkId=99934)합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="42caa-136">**DaRT 복구 이미지 마법사**를 실행 하는 컴퓨터에서 디버깅 도구의 위치를 지정 하거나 대상 컴퓨터에 있는 도구를 사용 하도록 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="42caa-137">다른 컴퓨터의 복사본을 사용 하기로 결정 한 경우에는 충돌을 진단 하는 각 컴퓨터에 도구가 설치 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="42caa-138">**참고**  ISO 이미지에 **충돌 분석기** 를 포함 하는 경우 Windows 용 디버깅 도구도 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="42caa-139">Windows 용 디버깅 도구를 추가 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="42caa-140">) 하이퍼링크를 클릭 하 여 Windows 용 디버깅 도구를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="42caa-141">다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="42caa-142">**다음 위치에서 Windows 용 디버깅 도구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="42caa-143">이 옵션을 선택 하면 도구의 위치로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="42caa-144">**복구 하려는 시스템에서 Windows 용 디버깅 도구를 찾습니다**.</span><span class="sxs-lookup"><span data-stu-id="42caa-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="42caa-145">이 옵션을 선택 하면 Windows 용 디버깅 도구가 문제 컴퓨터에 없는 경우 **충돌 분석기** 가 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="42caa-146">완료 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="42caa-147">DaRT 복구 이미지에 독립 실행형 시스템 Sweeper 대 한 정의를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="42caa-148">정의는 알려진 맬웨어 및 기타 잠재적으로 원치 않는 소프트웨어의 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="42caa-149">맬웨어는 지속적으로 개발 되 고 있기 때문에 **독립 실행형 시스템 Sweeper** 는 현재 정의에 따라 컴퓨터에서 설치, 실행 또는 설정을 변경 하려고 하는 소프트웨어가 잠재적으로 원치 않거나 악의적인 소프트웨어 인지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="42caa-150">DaRT 복구 이미지에 최신 정의를 포함 하려면 (권장) **예, 최신 정의를 다운로드 하세요.**</span><span class="sxs-lookup"><span data-stu-id="42caa-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="42caa-151">정의 업데이트가 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-151">The definition update starts automatically.</span></span> <span data-ttu-id="42caa-152">이 과정을 완료 하려면 인터넷에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="42caa-153">정의 업데이트를 건너뛰려면 **아니요를 클릭 하 고 나중에 수동으로 정의를 다운로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="42caa-154">정의는 DaRT 복구 이미지에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="42caa-155">복구 이미지에 최신 정의를 포함 하지 않기로 결정 하거나, **독립 실행형 시스템 Sweeper**를 사용할 준비가 된 시점에 복구 이미지에 포함 된 정의가 더 이상 유효 하지 않은 경우에는 **독립 실행형 시스템 Sweeper**에서 제공 하는 지침에 따라 검색을 시작 하기 전에 최신 정의를 구하십시오.</span><span class="sxs-lookup"><span data-stu-id="42caa-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="42caa-156">**중요**  정의가 없는 경우 스캔할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="42caa-157">완료 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="42caa-158">DaRT 복구 이미지에 드라이버 추가</span><span class="sxs-lookup"><span data-stu-id="42caa-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="42caa-159">**주의**  사항 기본적으로 DaRT 복구 이미지에 드라이버를 추가 하면 해당 폴더에 있는 모든 추가 파일 및 하위 폴더가 복구 이미지에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="42caa-160">자세한 내용은 [DaRT 7.0 문제 해결](troubleshooting-dart-70-new-ia.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="42caa-161">컴퓨터를 복구할 때 필요할 수 있는 DaRT7의 복구 이미지에 추가 드라이버를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="42caa-162">여기에는 일반적으로 Windows DVD에 포함 되지 않은 저장소 또는 네트워크 컨트롤러가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="42caa-163">**중요**  포함할 드라이버를 선택할 때 무선 연결이 DaRT에서 지원 되지 않는다는 점에 유의 하세요 (예: Bluetooth 또는 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="42caa-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="42caa-164">복구 이미지에 저장소 또는 네트워크 컨트롤러 드라이버를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="42caa-165">**DaRT 복구 이미지 마법사**의 **추가 드라이버** 대화 상자에서 **장치 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="42caa-166">드라이버에 추가할 파일을 찾은 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="42caa-167">**참고**  **드라이버** 파일은 저장소 또는 네트워크 컨트롤러의 제조업체에서 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="42caa-168">포함 하려는 모든 드라이버에 대해 1 ~ 2 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="42caa-169">완료 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="42caa-170">DaRT 복구 이미지에 파일을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="42caa-171">복구 이미지에 파일을 추가 하 여 컴퓨터 문제를 진단 하는 데 사용할 수 있도록 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="42caa-172">**DaRT 복구 이미지 마법사**의 **추가 파일** 대화 상자에서 **파일 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="42caa-173">이렇게 하면 공유 파일을 보유 하 고 있는 폴더가 표시 되는 탐색기 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="42caa-174">대화 상자에 나열 된 폴더에 하위 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="42caa-175">원하는 파일을 새 하위 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="42caa-176">완료 했으면 다음을 클릭 **합니다.**</span><span class="sxs-lookup"><span data-stu-id="42caa-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="42caa-177">DaRT 복구 이미지가 포함 된 ISO의 위치를 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="42caa-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="42caa-178">ISO 이미지를 만들 위치를 지정 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="42caa-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="42caa-179">**DaRT 복구 이미지 마법사**의 **시작 이미지 만들기** 대화 상자에서 **찾아보기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="42caa-180">다른 **이름으로 저장** 창에서 원하는 위치를 찾은 다음 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="42caa-181">완료 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="42caa-182">ISO 이미지의 크기는 사용자가 선택 하는 도구와 마법사에서 추가 하는 파일에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="42caa-183">CD 또는 DVD를 굽는 대부분의 프로그램에는 해당 확장이 필요 하기 때문에 마법사는 ISO 이미지에 .iso 파일 확장명을 사용 해야 합니다 **.**</span><span class="sxs-lookup"><span data-stu-id="42caa-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="42caa-184">다른 위치를 지정 하지 않으면 이름 **DaRT70**와 함께 바탕 화면에 iso 이미지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="42caa-185">CD 또는 DVD에 복구 이미지를 구우려면</span><span class="sxs-lookup"><span data-stu-id="42caa-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="42caa-186">**DaRT 복구 이미지 마법사** 가 컴퓨터에서 호환 되는 cd-rw 드라이브를 감지 하면 ISO 이미지를 디스크에 굽는 것을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="42caa-187">CD 또는 DVD를 구울 때 마법사에서 드라이브를 인식 하지 못하는 경우 드라이브에 포함 된 프로그램과 같은 다른 프로그램을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="42caa-188">Duplicator, 복제 서비스 또는 CD 또는 DVD 굽기 소프트웨어를 사용 하 여 추가 복사본을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="42caa-189">**DaRT 복구 이미지 마법사**의 **기록 가능한 CD/dvd로 굽기** 대화 상자에서 **기록 가능한 다음 CD/dvd 드라이브로 이미지 굽기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="42caa-190">CD 또는 DVD 드라이브를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="42caa-191">**참고**  드라이브가 인식 되지 않고 새 드라이브를 설치 하는 경우 **드라이브 목록 새로 고침** 을 클릭 하 여 마법사가 사용 가능한 드라이브 목록을 강제로 업데이트 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="42caa-192">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="42caa-192">Click **Next**.</span></span>

## <span data-ttu-id="42caa-193">관련 항목</span><span class="sxs-lookup"><span data-stu-id="42caa-193">Related topics</span></span>


[<span data-ttu-id="42caa-194">DaRT 7.0 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="42caa-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





