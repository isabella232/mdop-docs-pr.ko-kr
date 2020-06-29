---
title: DaRT 7.0 복구 이미지 만들기 계획
description: DaRT 7.0 복구 이미지 만들기 계획
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821333"
---
# <span data-ttu-id="7ee18-103">DaRT 7.0 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="7ee18-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="7ee18-104">이 섹션의 정보를 사용 하 여 Microsoft 진단 및 복구 도구 모음 (DaRT) 7 복구 이미지 만들기를 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="7ee18-105">DaRT 7 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="7ee18-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="7ee18-106">DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="7ee18-107">이러한 결정을 내릴 때는 최종 사용자가 다양 한 DaRT 도구에 액세스할 수 있다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="7ee18-108">DaRT 도구에 대 한 자세한 내용은 [dart 7.0의 도구 개요](overview-of-the-tools-in-dart-70-new-ia.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ee18-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="7ee18-109">보안 복구 이미지를 만드는 데 도움이 되는 방법에 대 한 자세한 내용은 [DaRT 7.0의 보안 고려 사항을](security-considerations-for-dart-70-dart-7.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ee18-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="7ee18-110">DaRT 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할 것인지 여부도 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="7ee18-111">DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="7ee18-112">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="7ee18-112">Prerequisites</span></span>


<span data-ttu-id="7ee18-113">DaRT 복구 이미지를 만들려면 다음 항목이 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="7ee18-114">Windows 7 원본 파일</span><span class="sxs-lookup"><span data-stu-id="7ee18-114">Windows 7 source files</span></span>

    <span data-ttu-id="7ee18-115">Windows 7 DVD 또는 Windows 7 원본 파일의 경로를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="7ee18-116">DaRT 복구 이미지를 만들려면 Windows 7 원본 파일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="7ee18-117">플랫폼용 Windows 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="7ee18-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="7ee18-118">Windows 디버깅 도구는 **충돌 분석기** 를 실행 하 여 컴퓨터 충돌 원인을 확인할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="7ee18-119">DaRT 복구 이미지를 만들 때 Windows 디버깅 도구의 경로를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="7ee18-120">필요한 경우 windows [용 디버깅 도구 다운로드 및 설치](https://go.microsoft.com/fwlink/?LinkId=99934)를 참조 하 여 Windows 디버깅 도구를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="7ee18-121">선택 사항: **독립 실행형 시스템 Sweeper** 정의</span><span class="sxs-lookup"><span data-stu-id="7ee18-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="7ee18-122">이 도구를 실행할 때 **독립 실행형 시스템 Sweeper** 에 대 한 최신 정의가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="7ee18-123">**독립 실행형 시스템 Sweeper**를 실행할 때 정의를 다운로드할 수 있지만 DaRT 복구 이미지를 만들 때 최신 정의를 다운로드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="7ee18-124">이 방법으로, 문제가 있는 컴퓨터에 네트워크 연결이 없는 경우에도 최신 정의로 도구를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="7ee18-125">선택 사항: **충돌 분석기** 에서 사용할 Windows 기호 파일</span><span class="sxs-lookup"><span data-stu-id="7ee18-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="7ee18-126">일반적으로 디버깅 정보는 실행 파일과는 별도의 기호 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="7ee18-127">충돌 하는 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee18-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="7ee18-128">자세한 내용은 [충돌 분석기를 사용 하 여 시스템 오류 진단을](diagnosing-system-failures-with-crash-analyzer--dart-7.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ee18-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="7ee18-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7ee18-129">Related topics</span></span>


[<span data-ttu-id="7ee18-130">DaRT 7.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="7ee18-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





