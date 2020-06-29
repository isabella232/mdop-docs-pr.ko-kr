---
title: Application Virtualization Sequencer 문제 해결
description: Application Virtualization Sequencer 문제 해결
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815183"
---
# <span data-ttu-id="37ef1-103">Application Virtualization Sequencer 문제 해결</span><span class="sxs-lookup"><span data-stu-id="37ef1-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="37ef1-104">이 항목에서는 Application Virtualization (App-v) Sequencer의 일반적인 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="37ef1-105">앱-V 시퀀서를 사용 하 여 SFTD 파일을 만들면 버전 번호가 예기치 않게 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="37ef1-106">SFTD 파일과 연결 된 버전 번호가 갑자기 늘어납니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="37ef1-107">해결 방법</span><span class="sxs-lookup"><span data-stu-id="37ef1-107">Solution</span></span>**

<span data-ttu-id="37ef1-108">명령줄을 사용 하 여 새 sft 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="37ef1-109">명령줄을 사용 하 여 sft 파일을 만들려면 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="37ef1-110">mkdiffpkg.exe &lt; 기본 sft 파일 이름 &gt; &lt; 차등 sft 파일 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="37ef1-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="37ef1-111">패키지 업그레이드 후 OSD 파일의 파일 이름이 올바르지 않음</span><span class="sxs-lookup"><span data-stu-id="37ef1-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="37ef1-112">기존 패키지를 업그레이드 한 후에는 파일 이름이 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="37ef1-113">해결 방법</span><span class="sxs-lookup"><span data-stu-id="37ef1-113">Solution</span></span>**

<span data-ttu-id="37ef1-114">업그레이드를 위해 패키지를 열 때 루트 Q:\\ 드라이브를 패키지의 출력 위치로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="37ef1-115">연결 된 파일 이름을 출력 위치와 함께 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="37ef1-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="37ef1-116">Microsoft Word2003 기본 설치로 인해 클라이언트로 스트리밍할 때 오류가 발생 하는 경우</span><span class="sxs-lookup"><span data-stu-id="37ef1-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="37ef1-117">Microsoft Word2003를 클라이언트로 스트리밍할 때 오류가 반환 되지만 Microsoft Word는 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="37ef1-118">해결 방법</span><span class="sxs-lookup"><span data-stu-id="37ef1-118">Solution</span></span>**

<span data-ttu-id="37ef1-119">가상 응용 프로그램 패키지를 Resequence 하 고 **전체 설치**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="37ef1-120">종속 패키지를 만들 때 패키지 업그레이드가 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="37ef1-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="37ef1-121">패키지 업그레이드를 사용 하 여 종속 패키지를 만들고 새 레지스트리 항목을 추가 하는 경우 올바르게 작동 하는 것 처럼 보이지만 업데이트 된 레지스트리 항목은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="37ef1-122">해결 방법</span><span class="sxs-lookup"><span data-stu-id="37ef1-122">Solution</span></span>**

<span data-ttu-id="37ef1-123">레지스트리 설정은 항상 패키지의 원본 버전과 함께 저장 되므로 원본 패키지를 복구 하지 않는 한 패키지에 대 한 업데이트는 사용할 수 없는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="37ef1-124">시퀀스를 시도 하는 동안 오류가 발생 했습니다. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="37ef1-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="37ef1-125">필요한 패키지를 시퀀싱 하는 경우 NET 2.0을 시작 하면 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="37ef1-126">해결 방법</span><span class="sxs-lookup"><span data-stu-id="37ef1-126">Solution</span></span>**

<span data-ttu-id="37ef1-127">필요한 시퀀싱 패키지 NET 2.0은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ef1-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="37ef1-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="37ef1-128">Related topics</span></span>


[<span data-ttu-id="37ef1-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="37ef1-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





