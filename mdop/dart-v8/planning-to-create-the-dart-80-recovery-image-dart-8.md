---
title: DaRT 8.0 복구 이미지 만들기 계획
description: DaRT 8.0 복구 이미지 만들기 계획
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824808"
---
# <span data-ttu-id="7e5e6-103">DaRT 8.0 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="7e5e6-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="7e5e6-104">이 섹션의 정보를 사용 하 여 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="7e5e6-105">DaRT 8.0 복구 이미지 만들기 계획</span><span class="sxs-lookup"><span data-stu-id="7e5e6-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="7e5e6-106">DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="7e5e6-107">이를 결정 하려면 최종 사용자가 해당 도구에 액세스할 수 있다는 것을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="7e5e6-108">지원 엔지니어가 최종 사용자의 컴퓨터에 복구 이미지 미디어를 사용 하 여 문제를 진단 하는 경우 복구 이미지에 모든 도구를 설치 하는 것이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="7e5e6-109">최종 사용자의 컴퓨터를 원격으로 진단할 계획 이라면 디스크 지우기 및 레지스트리 편집기와 같은 일부 도구를 사용 하지 않도록 설정 하 고 원격 연결을 비롯 한 다른 도구를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="7e5e6-110">DaRT 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할 것인지 여부도 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="7e5e6-111">DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="7e5e6-112">DaRT 도구에 대 한 자세한 내용은 [dart 8.0의 도구 개요](overview-of-the-tools-in-dart-80-dart-8.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="7e5e6-113">보안 복구 이미지를 만드는 데 도움이 되는 방법에 대 한 자세한 내용은 [DaRT 8.0의 보안 고려 사항을](security-considerations-for-dart-80--dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="7e5e6-114">복구 이미지에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="7e5e6-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="7e5e6-115">DaRT 복구 이미지를 만들려면 다음 항목이 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7e5e6-116">요소일</span><span class="sxs-lookup"><span data-stu-id="7e5e6-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7e5e6-117">세부 정보</span><span class="sxs-lookup"><span data-stu-id="7e5e6-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e5e6-118">Windows 8 원본 파일</span><span class="sxs-lookup"><span data-stu-id="7e5e6-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e5e6-119">DaRT 복구 이미지를 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="7e5e6-120">Windows 8 DVD 또는 Windows 8 원본 파일의 경로를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e5e6-121">플랫폼용 Windows 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="7e5e6-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e5e6-122"><strong>충돌 분석기를 실행 </strong> 하 여 컴퓨터 오류의 원인을 확인할 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="7e5e6-123">DaRT 복구 이미지를 만들 때 Windows 디버깅 도구의 경로를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="7e5e6-124">Windows 디버깅 도구를 다운로드 <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> 하 고 windows 용 디버깅 도구를 설치할 수 있습니다. </a></span><span class="sxs-lookup"><span data-stu-id="7e5e6-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e5e6-125">선택 사항: <strong> Defender </strong> 정의</span><span class="sxs-lookup"><span data-stu-id="7e5e6-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e5e6-126">Defender를 <strong> 실행할 때 defender에 대 한 최신 정의가 </strong> 필요 합니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="7e5e6-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="7e5e6-127">Defender를 실행할 때 정의를 다운로드할 수 있지만 <strong> </strong> , 문제가 있는 컴퓨터에 네트워크 연결이 없는 경우에도 최신 정의로 도구를 계속 실행할 수 있도록 DaRT 복구 이미지를 만들 때 최신 정의를 다운로드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e5e6-128">선택 사항: 충돌 분석기에서 사용할 Windows 기호 파일 <strong></span><span class="sxs-lookup"><span data-stu-id="7e5e6-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7e5e6-129">일반적으로 디버깅 정보는 프로그램과는 별도의 기호 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="7e5e6-130">작업이 중지 된 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="7e5e6-131">자세한 내용은 <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> 충돌 분석기를 사용 하 여 시스템 오류 진단을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="7e5e6-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7e5e6-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7e5e6-132">Related topics</span></span>


[<span data-ttu-id="7e5e6-133">DaRT 8.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="7e5e6-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





