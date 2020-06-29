---
title: Application Virtualization Sequencer 문제 해결
description: Application Virtualization Sequencer 문제 해결
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815243"
---
# <span data-ttu-id="0eac3-103">Application Virtualization Sequencer 문제 해결</span><span class="sxs-lookup"><span data-stu-id="0eac3-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="0eac3-104">이 항목에서는 Application Virtualization (App-v) Sequencer의 일반적인 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="0eac3-105">앱-V 시퀀서를 사용 하 여 SFTD 파일을 만들면 버전 번호가 예기치 않게 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="0eac3-106">명령줄을 사용 하 여 새 sft 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="0eac3-107">명령줄을 사용 하 여 sft 파일을 만들려면 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="0eac3-108">mkdiffpkg.exe &lt; 기본 sft 파일 이름 &gt; &lt; 차등 sft 파일 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="0eac3-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="0eac3-109">패키지 업그레이드 후 OSD 파일의 파일 이름이 올바르지 않음</span><span class="sxs-lookup"><span data-stu-id="0eac3-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="0eac3-110">업그레이드를 위해 패키지를 열 때 루트 Q:\\ 드라이브를 패키지의 출력 위치로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="0eac3-111">연결 된 파일 이름을 출력 위치와 함께 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0eac3-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="0eac3-112">Microsoft Word2003 기본 설치로 인해 클라이언트로 스트리밍할 때 오류가 발생 하는 경우</span><span class="sxs-lookup"><span data-stu-id="0eac3-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="0eac3-113">Microsoft Word2003를 클라이언트로 스트리밍할 때 오류가 반환 되지만 Microsoft Word는 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="0eac3-114">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0eac3-114">Solution</span></span>**

<span data-ttu-id="0eac3-115">가상 응용 프로그램 패키지를 Resequence 하 고 **전체 설치**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="0eac3-116">종속 패키지를 만들 때 활성 업그레이드가 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="0eac3-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="0eac3-117">활성 업그레이드를 사용 하 여 종속 패키지를 만들고 새 레지스트리 항목을 추가 하는 경우 올바르게 작동 하는 것 처럼 보이지만 업데이트 된 레지스트리 항목은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="0eac3-118">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0eac3-118">Solution</span></span>**

<span data-ttu-id="0eac3-119">레지스트리 설정은 항상 패키지의 원본 버전과 함께 저장 되므로 원본 패키지를 복구 하지 않는 한 패키지에 대 한 업데이트는 사용할 수 없는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="0eac3-120">속성 페이지를 사용 하 여 Microsoft Office2007 문서에 대 한 자세한 정보가 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="0eac3-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="0eac3-121">속성 페이지를 사용 하 여 Microsoft Office2007 문서와 관련 된 세부 정보를 보려고 하면 자세한 정보가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="0eac3-122">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0eac3-122">Solution</span></span>**

<span data-ttu-id="0eac3-123">App-v는 이러한 속성 페이지에 필요한 셸 확장을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="0eac3-124">16 비트 응용 프로그램을 시퀀싱 할 때 일부 레지스트리 키가 캡처되지 않음</span><span class="sxs-lookup"><span data-stu-id="0eac3-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="0eac3-125">App-v 4.5에서 레지스트리 후크는 커널 모드에서 사용자 모드로 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="0eac3-126">16 비트 응용 프로그램이 나 16 비트 설치 관리자를 사용 하는 응용 프로그램을 시퀀싱 하려면 먼저 Windows NT NTVDM (가상 DOS 시스템)의 고유한 복사본에서 프로세스가 실행 되도록 sequencer 컴퓨터를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="0eac3-127">해결 방법</span><span class="sxs-lookup"><span data-stu-id="0eac3-127">Solution</span></span>**

<span data-ttu-id="0eac3-128">응용 프로그램을 순서 대로 설정 하기 전에 시퀀싱 컴퓨터에서 다음과 같은 전역 REGSZ 레지스트리 키 값을 "yes"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="0eac3-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="0eac3-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="0eac3-130">이 효과를 적용 하려면 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eac3-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="0eac3-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0eac3-131">Related topics</span></span>


[<span data-ttu-id="0eac3-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0eac3-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





