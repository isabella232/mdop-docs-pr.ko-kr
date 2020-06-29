---
title: MED-V에 대한 Windows 가상 PC 이미지 만들기
description: MED-V에 대한 Windows 가상 PC 이미지 만들기
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812684"
---
# <span data-ttu-id="9770b-103">MED-V에 대한 Windows 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="9770b-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="9770b-104">MED-V 작업 영역을 사용자에 게 제공 하기 전에 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에 대 한 MED-V 작업 영역 설치 관리자 패키지를 빌드하는 데 사용 하는 가상 하드 디스크를 먼저 준비 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="9770b-105">필요한 가상 하드 디스크를 준비 하려면 나중에 응용 프로그램 및 URL 리디렉션 정보를 사용자에 게 배포할 수 있도록 필요한 운영 체제, 업데이트 및 소프트웨어를 포함 하는 Windows 가상 PC 이미지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="9770b-106">이 섹션에서는 가상 하드 디스크를 만드는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="9770b-107">MED-V에 대 한 가상 이미지를 만들려면 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="9770b-108">Windows 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="9770b-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="9770b-109">이미지에 Windows XP 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="9770b-110">이미지에 .NET Framework 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="9770b-111">이미지에 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="9770b-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="9770b-112">통합 구성 요소 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="9770b-113">Windows 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="9770b-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="9770b-114">Windows 가상 PC 이미지를 만들려면 Windows 가상 PC 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9770b-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="9770b-115">[Windows 가상 PC 홈 페이지](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="9770b-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="9770b-116">[Windows 가상 PC 도움말](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="9770b-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="9770b-117">또는 가상 이미지의 기준으로 사용할 Windows Imaging (WIM) 파일이 이미 있는 경우이를 MED-V 작업 영역을 빌드하는 데 사용 하는 VHD로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="9770b-118">WIM을 가상 하드 디스크로 변환 하는 방법에 대 한 자세한 내용은 [Windows 7 ()의 기본 VHD 지원](https://go.microsoft.com/fwlink/?LinkId=195922) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="9770b-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="9770b-119">**중요**  MED-V는 가상 컴퓨터당 하나의 가상 하드 디스크만 지원 하 고 각 가상 디스크에는 하나의 파티션만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="9770b-120">가상 하드 디스크를 만들었으면 이미지에 Windows XP를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="9770b-121">Windows 가상 PC 이미지에 Windows XP 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="9770b-122">MED-V를 사용 하려면 MED-V 작업 영역을 빌드하기 전에 windows XP SP3이 Windows 가상 PC 이미지에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="9770b-123">Windows XP를 설치 하는 방법에 대 한 자세한 내용은 [가상 컴퓨터 만들기 및 게스트 운영 체제 설치](https://go.microsoft.com/fwlink/?LinkId=182379) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="9770b-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="9770b-124">Windows 가상 PC 이미지에 .NET Framework 3.5 SP1 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="9770b-125">.NET Framework 3.5 SP1 및 업데이트 KB959209을 MED-V와 함께 사용 하기 위해 준비 하는 Windows 가상 PC 이미지에 수동으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="9770b-126">업데이트 [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) 알려진 여러 응용 프로그램 호환성 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="9770b-127">Windows 가상 PC 이미지에 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="9770b-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="9770b-128">가상 컴퓨터에 Windows XP를 설치한 후에는 SP3 등의 이미지에 필요한 Windows XP 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="9770b-129">더 나은 성능을 위해 특정 선택적 업데이트를 설치할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="9770b-130">**중요**  MED-V를 사용 하려면 게스트 운영 체제에서 Windows XP SP3을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="9770b-131">**경고가**  Windows XP에 대 한 업데이트를 설치 하는 경우 MED-V 작업 영역에서 사용 하려는 게스트의 Internet Explorer 버전에 남아 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="9770b-132">예를 들어 MED-V 작업 영역에서 Internet Explorer 6을 실행 하려는 경우 지금 설치 하는 업데이트에는 Internet Explorer 7 또는 Internet Explorer 8이 포함 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="9770b-133">또한 자동 업데이트가 Internet Explorer를 업그레이드 하지 못하도록 레지스트리를 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="9770b-134">선택적 성능 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="9770b-135">이 기능은 선택 사항 이지만 [핫픽스 KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ()에 대해 다음 업데이트를 설치 하는 것이 좋습니다 https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="9770b-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="9770b-136">이 업데이트는 터미널 서비스 세션에서 공유 폴더의 성능을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="9770b-137">**참고**  업데이트를 공개적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="9770b-138">그러나 Microsoft 서비스에 대 한 계약을 수락 하 라는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="9770b-139">후속 웹 페이지의 메시지에 따라이 핫픽스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="9770b-140">그룹 정책 성능 업데이트 구성</span><span class="sxs-lookup"><span data-stu-id="9770b-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="9770b-141">기본적으로 그룹 정책은 한 번에 1 바이트씩 컴퓨터에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="9770b-142">이로 인해 MED-V가 도메인에 가입 되어 있는 동안 지연이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="9770b-143">그룹 정책의 성능을 높이려면 다음 레지스트리 키 값을 레지스트리로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="9770b-144">레지스트리 하위 키: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="9770b-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="9770b-145">진입: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="9770b-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="9770b-146">형식: DWORD</span><span class="sxs-lookup"><span data-stu-id="9770b-146">Type: DWORD</span></span>

<span data-ttu-id="9770b-147">값: 1</span><span class="sxs-lookup"><span data-stu-id="9770b-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="9770b-148">통합 구성 요소 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-148">Installing Integration Components</span></span>


<span data-ttu-id="9770b-149">Windows 가상 PC에는 통합 구성 요소 패키지가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="9770b-150">가상 환경과 물리적 컴퓨터 간의 상호 작용을 개선 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="9770b-151">예를 들어 통합 구성 요소 패키지는 마우스를 호스트와 게스트 컴퓨터 간에 이동할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="9770b-152">**중요**  MED-V는 통합 구성 요소 패키지를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="9770b-153">MED-V와 함께 작동 하도록 가상 이미지를 구성 하는 경우 게스트 운영 체제에 통합 구성 요소 패키지를 수동으로 설치 하 여 통합 기능을 사용할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="9770b-154">통합 구성 요소 패키지를 설치 하 고 사용 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9770b-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="9770b-155">[통합 구성 요소 패키지 설치 또는 업그레이드](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="9770b-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="9770b-156">[통합 기능](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="9770b-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="9770b-157">RemoteApp 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="9770b-158">통합 구성 요소 패키지를 설치한 후 다음 업데이트를 설치 하 라는 메시지가 표시 됩니다. "Windows XP SP3 용 업데이트: RemoteApp 사용"</span><span class="sxs-lookup"><span data-stu-id="9770b-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="9770b-159">이는 MED-V에 필요한 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="9770b-160">**중요**  RemoteApp 업데이트를 설치 하 라는 메시지가 표시 되지 않는 경우 수동으로 다운로드 하 여 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="9770b-161">이 업데이트를 다운로드 하는 방법에 대 한 자세한 내용과 지침은 [RemoteApp을 사용 하도록 설정 하는 WINDOWS XP SP3 업데이트](https://go.microsoft.com/fwlink/?LinkId=195925) (.)를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="9770b-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="9770b-162">원격 데스크톱 사용</span><span class="sxs-lookup"><span data-stu-id="9770b-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="9770b-163">통합 구성 요소 패키지를 설치한 후 원격 데스크톱이 기본적으로 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="9770b-164">MED-V가 작동 하도록 하려면 원격 데스크톱을 사용 하도록 설정 하 고 사용 하지 않도록 설정 하는 그룹 정책을 배포 하지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="9770b-165">원격 데스크톱을 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [원격 데스크톱 사용 또는 사용 안 함](https://go.microsoft.com/fwlink/?LinkId=201162) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="9770b-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="9770b-166">Internet Explorer 관리 키트를 사용 하 여 Internet Explorer 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="9770b-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="9770b-167">원하는 경우 Internet Explorer 관리 키트를 사용 하 여 게스트 운영 체제에서 Internet Explorer를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="9770b-168">자세한 내용은 [Internet Explorer 6 관리 키트 및 배포 가이드](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.microsoft.com/fwlink/?LinkId=200007)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9770b-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="9770b-169">**경고가**  MED-V 작업 영역에서 Internet Explorer를 사용자 지정 하는 것과 관련 된 보안 문제를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="9770b-170">자세한 내용은 [Med-v 작업에 대 한 보안 모범 사례](security-best-practices-for-med-v-operations.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9770b-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="9770b-171">가상 하드 디스크가 최신 게스트 운영 체제로 설치 되 면 이미지에 응용 프로그램을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9770b-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="9770b-172">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9770b-172">Related topics</span></span>


[<span data-ttu-id="9770b-173">Windows 가상 PC 이미지에 응용 프로그램 설치</span><span class="sxs-lookup"><span data-stu-id="9770b-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="9770b-174">MED-V에 대한 Windows 가상 PC 이미지 구성</span><span class="sxs-lookup"><span data-stu-id="9770b-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





