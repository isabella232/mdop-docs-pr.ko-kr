---
title: 크래시 분석기를 사용하여 시스템 오류 진단
description: 크래시 분석기를 사용하여 시스템 오류 진단
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824543"
---
# <span data-ttu-id="373ee-103">크래시 분석기를 사용하여 시스템 오류 진단</span><span class="sxs-lookup"><span data-stu-id="373ee-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="373ee-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0의 **충돌 분석기** 를 사용 하 여 Windows 기반 컴퓨터에서 메모리 덤프 파일을 디버그 하 고 관련 컴퓨터 오류를 진단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="373ee-105">**충돌 분석기** 는 Windows 용 Microsoft 디버깅 도구를 사용 하 여 컴퓨터에 오류가 발생 한 드라이버에 대 한 메모리 덤프 파일을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="373ee-106">최종 사용자 컴퓨터 또는 최종 사용자 컴퓨터가 아닌 컴퓨터의 독립 실행형 모드에서 충돌 분석기를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="373ee-107">최종 사용자 컴퓨터에서 충돌 분석기 실행</span><span class="sxs-lookup"><span data-stu-id="373ee-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="373ee-108">일반적으로 문제가 발생 하는 최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="373ee-109">**충돌 분석기** 는 문제 컴퓨터에서 Windows 용 디버깅 도구를 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="373ee-110">디렉터리 경로 대화 상자가 비어 있는 경우에는 위치를 입력 하거나 Windows 용 디버깅 도구 (Microsoft에서 파일을 다운로드할 수 있음)의 위치를 탐색 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="373ee-111">또한 기호 파일이 있는 위치에 대 한 경로도 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="373ee-112">Windows 용 Microsoft 디버깅 도구를 포함 하 고 있으며 DaRT 8.0 복구 이미지를 만들 때 기호 파일을 추가한 경우에는 문제 컴퓨터에서 **충돌 분석기** 를 실행할 때 도구 및 기호 파일을 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="373ee-113">DaRT 복구 이미지에 포함 하지 않았거나 디스크 크기 또는 네트워크 연결 문제로 인해이를 가져올 수 없는 경우 다음 섹션에서 설명 하는 대로 최종 사용자의 컴퓨터가 아닌 다른 컴퓨터의 독립 실행형 모드에서 충돌 분석기를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="373ee-114">최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="373ee-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="373ee-115">최종 사용자의 컴퓨터가 아닌 컴퓨터에서 독립 실행형 모드로 충돌 분석기 실행</span><span class="sxs-lookup"><span data-stu-id="373ee-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="373ee-116">일반적으로 문제가 발생 하는 최종 사용자 컴퓨터에서 **충돌 분석기** 를 실행 하지만 최종 사용자 컴퓨터가 아닌 컴퓨터에서 독립 실행형 모드의 충돌 분석기를 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="373ee-117">DaRT 복구 이미지에 Windows 디버깅 도구를 포함 하지 않았거나 디스크 크기 또는 네트워크 연결 문제로 인해 디버깅 도구를 가져오지 못하는 경우이 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="373ee-118">이 경우 문제 컴퓨터에서 덤프 파일을 복사 하 고 지원 센터 에이전트 컴퓨터와 같이 독립 실행형 버전의 **크래시 분석기** 가 설치 된 컴퓨터에서이를 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="373ee-119">최종 사용자 컴퓨터 이외의 컴퓨터에서 독립 실행형 모드로 크래시 분석기를 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="373ee-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="373ee-120">충돌 분석기가 기호 파일에 액세스할 수 있는지 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="373ee-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="373ee-121">응답을 중지 한 응용 프로그램을 디버깅 하려면 프로그램에서 분리 된 기호 파일에 대 한 액세스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="373ee-122">충돌 분석기를 실행할 때 기호 파일은 자동으로 다운로드 되지만, 문제가 있는 컴퓨터에서 인터넷에 액세스할 수 없는 경우도 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="373ee-123">기호 파일에 대 한 액세스를 보장 하는 방법에는 여러 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="373ee-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="373ee-124">크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법</span><span class="sxs-lookup"><span data-stu-id="373ee-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="373ee-125">충돌 분석기를 사용 하 여 시스템 오류를 진단 하는 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="373ee-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="373ee-126">DaRT 8.0 작업</span><span class="sxs-lookup"><span data-stu-id="373ee-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





