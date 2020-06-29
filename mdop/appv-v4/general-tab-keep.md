---
title: 일반 탭
description: 일반 탭
author: dansimp
ms.assetid: aeefae39-60cd-4ad4-9575-c07d7e2b1e59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 327635422030b713aeadbc5de0007685b69e1c2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821473"
---
# <span data-ttu-id="e8c9e-103">일반 탭</span><span class="sxs-lookup"><span data-stu-id="e8c9e-103">General Tab</span></span>


<span data-ttu-id="e8c9e-104">**일반** 탭을 사용 하 여 Microsoft Application Virtualization (App-v) 시퀀서에 대 한 옵션을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-104">Use the **General** tab to configure options for Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<a href="" id="scratch-directory"></a>**<span data-ttu-id="e8c9e-105">스크래치 디렉터리</span><span class="sxs-lookup"><span data-stu-id="e8c9e-105">Scratch Directory</span></span>**  
<span data-ttu-id="e8c9e-106">시퀀싱 하는 동안 생성 되는 파일을 일시적으로 저장할 위치에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-106">Specifies the path to the location where the Sequencer will temporarily save files generated during sequencing.</span></span> <span data-ttu-id="e8c9e-107">기본 경로는 C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Scratch.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-107">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Scratch.</span></span> <span data-ttu-id="e8c9e-108">새 경로를 지정 하려면 **찾아보기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-108">To specify a new path, click **Browse**.</span></span>

<a href="" id="log-directory"></a>**<span data-ttu-id="e8c9e-109">로그 디렉터리</span><span class="sxs-lookup"><span data-stu-id="e8c9e-109">Log Directory</span></span>**  
<span data-ttu-id="e8c9e-110">Sequencer에서 로그 파일을 저장할 디렉터리 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-110">Specifies the path to the directory where the Sequencer will save log files.</span></span> <span data-ttu-id="e8c9e-111">기본 경로는 C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Logs.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-111">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Logs.</span></span> <span data-ttu-id="e8c9e-112">새 경로를 지정 하려면 **찾아보기를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-112">To specify a new path, click **Browse**</span></span>

<a href="" id="allow-use-of-msi-installer"></a>**<span data-ttu-id="e8c9e-113">MSI 설치 관리자의 사용 허용</span><span class="sxs-lookup"><span data-stu-id="e8c9e-113">Allow Use of MSI Installer</span></span>**  
<span data-ttu-id="e8c9e-114">Sequencer와 응용 프로그램 설치 관리자 간의 상호 작용을 허용 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-114">Select this option to allow interaction between the Sequencer and the application installer.</span></span> <span data-ttu-id="e8c9e-115">이 옵션은 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-115">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-events"></a>**<span data-ttu-id="e8c9e-116">이벤트 가상화 허용</span><span class="sxs-lookup"><span data-stu-id="e8c9e-116">Allow Virtualization of Events</span></span>**  
<span data-ttu-id="e8c9e-117">이 옵션을 선택 하면 응용 프로그램의 하위 수준 운영 체제 작업을 App-v 데스크톱 클라이언트에서 실행 하는 경우 시퀀싱 된 응용 프로그램 패키지가 가상화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-117">Select this option to allow low-level operating system activities of the application to be virtualized when a sequenced application package is run on App-V Desktop Clients.</span></span> <span data-ttu-id="e8c9e-118">이 옵션은 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-118">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-services"></a>**<span data-ttu-id="e8c9e-119">서비스 가상화 허용</span><span class="sxs-lookup"><span data-stu-id="e8c9e-119">Allow Virtualization of Services</span></span>**  
<span data-ttu-id="e8c9e-120">앱이 App-v 데스크톱 클라이언트에서 실행 될 때 응용 프로그램을 가상화 하기 위해 필요한 서비스를 허용 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-120">Select this option to allow services required by the application to be virtualized when the application is run on App-V Desktop Clients.</span></span> <span data-ttu-id="e8c9e-121">이 옵션은 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-121">This option is selected by default.</span></span>

<a href="" id="append-package-version-to-filename"></a>**<span data-ttu-id="e8c9e-122">패키지 버전을 파일 이름에 추가</span><span class="sxs-lookup"><span data-stu-id="e8c9e-122">Append Package Version to Filename</span></span>**  
<span data-ttu-id="e8c9e-123">시퀀싱 된 응용 프로그램 패키지 버전 번호를 파일 이름에 자동으로 추가 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-123">Select this option to automatically append the sequenced application package version number to the file name.</span></span> <span data-ttu-id="e8c9e-124">이 옵션은 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-124">This option is selected by default.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="e8c9e-125">확인</span><span class="sxs-lookup"><span data-stu-id="e8c9e-125">OK</span></span>**  
<span data-ttu-id="e8c9e-126">변경 내용을 저장 하 고 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-126">Saves changes and closes the dialog box.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="e8c9e-127">취소</span><span class="sxs-lookup"><span data-stu-id="e8c9e-127">Cancel</span></span>**  
<span data-ttu-id="e8c9e-128">변경 내용을 저장 하지 않고 대화 상자를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-128">Exits the dialog box without saving any changes.</span></span>

<a href="" id="apply"></a>**<span data-ttu-id="e8c9e-129">적용</span><span class="sxs-lookup"><span data-stu-id="e8c9e-129">Apply</span></span>**  
<span data-ttu-id="e8c9e-130">변경 내용을 저장 하 고 대화 상자에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c9e-130">Saves the changes and remains in the dialog box.</span></span>

## <span data-ttu-id="e8c9e-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8c9e-131">Related topics</span></span>


[<span data-ttu-id="e8c9e-132">Application Virtualization Sequencer 옵션 대화 상자</span><span class="sxs-lookup"><span data-stu-id="e8c9e-132">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

 

 





