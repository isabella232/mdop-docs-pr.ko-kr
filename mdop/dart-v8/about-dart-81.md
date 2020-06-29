---
title: DaRT 8.1 정보
description: DaRT 8.1 정보
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821263"
---
# <span data-ttu-id="94471-103">DaRT 8.1 정보</span><span class="sxs-lookup"><span data-stu-id="94471-103">About DaRT 8.1</span></span>


<span data-ttu-id="94471-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.1은 다음과 같은 향상 된 기능을 제공 합니다 .이 항목에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="94471-105">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="94471-105">What’s new</span></span>


-   **<span data-ttu-id="94471-106">WIMBoot에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="94471-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="94471-107">진단 및 복구 도구 집합 8.1는 다음 조건이 충족 되는 경우 Windows 이미지 파일 부팅 (WIMBoot) 환경을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="94471-108">WIMBoot는 Windows 8.1 업데이트 1 이상을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="94471-109">DaRT 8.1 이미지는 Windows 8.1 업데이트 1 이상에서 작성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="94471-110">WIMBoot에 대 한 자세한 내용은 [Windows 이미지 파일 부팅 (WIMBoot) 개요](https://go.microsoft.com/fwlink/?LinkId=517536)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94471-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="94471-111">Windows Server 2012 R2 및 Windows 8.1에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="94471-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="94471-112">Windows Server 2012 R2 또는 Windows 8.1를 사용 하 여 DaRT 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="94471-113">참고</span><span class="sxs-lookup"><span data-stu-id="94471-113">Note</span></span>**  
    <span data-ttu-id="94471-114">이전 버전의 Windows Server 및 Windows 운영 체제에서는 이전 버전의 DaRT를 계속 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="94471-115">고객 피드백</span><span class="sxs-lookup"><span data-stu-id="94471-115">Customer feedback</span></span>**

    <span data-ttu-id="94471-116">DaRT 8.1에는 DaRT 8.0 SP1 릴리스 이후 발견 된 문제를 해결 하는 업데이트가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="94471-117">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="94471-117">Windows Defender</span></span>**

    <span data-ttu-id="94471-118">Windows 8.1의 windows Defender에는 향상 된 보호가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="94471-119">변경 사항은 Windows Defender에 DaRT를 사용 하는 방법에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="94471-120">요구 사항</span><span class="sxs-lookup"><span data-stu-id="94471-120">Requirements</span></span>


-   **<span data-ttu-id="94471-121">Windows 평가 및 개발 키트 8.1</span><span class="sxs-lookup"><span data-stu-id="94471-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="94471-122">Windows ADK (평가 및 개발 키트) 8.1는 DaRT 복구 이미지 마법사의 필수 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="94471-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="94471-123">Windows ADK 8.1에는 Windows 이미지를 사용자 지정, 배포 및 서비스 하는 데 사용 되는 배포 도구가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="94471-124">Windows PE (Windows 사전 설치 환경)도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="94471-125">참고</span><span class="sxs-lookup"><span data-stu-id="94471-125">Note</span></span>**  
    <span data-ttu-id="94471-126">원격 연결 뷰어 또는 충돌 분석기만 설치 하는 경우 Windows ADK 8.1이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94471-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="94471-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="94471-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="94471-128">DaRT 8.1에는 .NET Framework 4.5.1이 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="94471-129">다운로드 하려면 Microsoft 다운로드 센터에서 [Microsoft.NET 프레임 워크 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94471-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="94471-130">Windows 8.1 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="94471-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="94471-131">DaRT 8.1에서 충돌 분석기 도구를 사용 하려면 Windows 8.1 용 소프트웨어 개발 키트에서 사용할 수 있는 필수 디버깅 도구가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="94471-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="94471-132">다운로드 하려면 Microsoft 다운로드 센터에서 [windows 8.1 용 WINDOWS SDK (소프트웨어 개발 키트)](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94471-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="94471-133">언어 가용성</span><span class="sxs-lookup"><span data-stu-id="94471-133">Language availability</span></span>


<span data-ttu-id="94471-134">DaRT 8.1는 다음 언어로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94471-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="94471-135">영어 (미국) en-us-US</span><span class="sxs-lookup"><span data-stu-id="94471-135">English (United States) en-US</span></span>

-   <span data-ttu-id="94471-136">프랑스어 (프랑스) fr-fr</span><span class="sxs-lookup"><span data-stu-id="94471-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="94471-137">이탈리아어 (이탈리아) it</span><span class="sxs-lookup"><span data-stu-id="94471-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="94471-138">독일어 (독일) DE-DE</span><span class="sxs-lookup"><span data-stu-id="94471-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="94471-139">스페인어, 국제 정렬 (스페인-ES)</span><span class="sxs-lookup"><span data-stu-id="94471-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="94471-140">한국어 (대한민국) ko-kr-KR</span><span class="sxs-lookup"><span data-stu-id="94471-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="94471-141">일본어 (일본) ja-jp</span><span class="sxs-lookup"><span data-stu-id="94471-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="94471-142">포르투갈어 (브라질) pt-BR</span><span class="sxs-lookup"><span data-stu-id="94471-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="94471-143">러시아어 (러시아)의 기능</span><span class="sxs-lookup"><span data-stu-id="94471-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="94471-144">중국어 번체 zh-cn-hy 얕은 샘물 a</span><span class="sxs-lookup"><span data-stu-id="94471-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="94471-145">중국어 간체 zh-cn-CN</span><span class="sxs-lookup"><span data-stu-id="94471-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="94471-146">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="94471-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="94471-147">DaRT 8.1는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="94471-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="94471-148">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="94471-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="94471-149">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="94471-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="94471-150">관련 항목</span><span class="sxs-lookup"><span data-stu-id="94471-150">Related topics</span></span>


[<span data-ttu-id="94471-151">DaRT 8.1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="94471-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









