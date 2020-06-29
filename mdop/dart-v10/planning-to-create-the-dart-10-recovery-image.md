---
title: DaRT 10 복구 이미지 만들기 계획
description: DaRT 10 복구 이미지 만들기 계획
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822978"
---
# <span data-ttu-id="980c3-103">DaRT 10 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="980c3-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="980c3-104">이 섹션의 정보를 사용 하 여 Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지를 만들 계획을 세울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="980c3-105">DaRT 10 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="980c3-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="980c3-106">DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="980c3-107">이를 결정 하려면 최종 사용자가 해당 도구에 액세스할 수 있다는 것을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="980c3-108">지원 엔지니어가 최종 사용자의 컴퓨터에 복구 이미지 미디어를 사용 하 여 문제를 진단 하는 경우 복구 이미지에 모든 도구를 설치 하는 것이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="980c3-109">최종 사용자의 컴퓨터를 원격으로 진단할 계획 이라면 디스크 지우기 및 레지스트리 편집기와 같은 일부 도구를 사용 하지 않도록 설정 하 고 원격 연결을 비롯 한 다른 도구를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="980c3-110">DaRT 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할 것인지 여부도 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="980c3-111">DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="980c3-112">DaRT 도구에 대 한 자세한 내용은 [dart 10의 도구 개요](overview-of-the-tools-in-dart-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="980c3-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="980c3-113">보안 복구 이미지를 만드는 데 도움이 되는 방법에 대 한 자세한 내용은 [DaRT 10의 보안 고려 사항을](security-considerations-for-dart-10.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="980c3-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="980c3-114">복구 이미지에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="980c3-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="980c3-115">DaRT 복구 이미지를 만들려면 다음 항목이 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="980c3-116">요소일</span><span class="sxs-lookup"><span data-stu-id="980c3-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="980c3-117">세부 정보</span><span class="sxs-lookup"><span data-stu-id="980c3-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="980c3-118">Windows 10 원본 파일</span><span class="sxs-lookup"><span data-stu-id="980c3-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="980c3-119">DaRT 복구 이미지를 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="980c3-120">Windows 10 DVD 또는 Windows 10 원본 파일의 경로를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="980c3-121">플랫폼용 Windows 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="980c3-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="980c3-122"><strong>충돌 분석기를 실행 </strong> 하 여 컴퓨터 오류의 원인을 확인할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="980c3-123">DaRT 복구 이미지를 만들 때 Windows 디버깅 도구의 경로를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="980c3-124">Windows 디버깅 도구를 다운로드 <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> 하 고 windows 용 디버깅 도구를 설치할 수 있습니다. </a></span><span class="sxs-lookup"><span data-stu-id="980c3-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="980c3-125">선택 사항: 충돌 분석기에서 사용할 Windows 기호 파일 <strong></span><span class="sxs-lookup"><span data-stu-id="980c3-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="980c3-126">일반적으로 디버깅 정보는 프로그램과는 별도의 기호 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="980c3-127">작업이 중지 된 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="980c3-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="980c3-128">자세한 내용은 <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> 충돌 분석기를 사용 하 여 시스템 오류 진단을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="980c3-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="980c3-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="980c3-129">Related topics</span></span>

[<span data-ttu-id="980c3-130">DaRT 10 배포 계획</span><span class="sxs-lookup"><span data-stu-id="980c3-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




