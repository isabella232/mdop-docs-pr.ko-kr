---
title: Application Virtualization Sequencer Console 개요
description: Application Virtualization Sequencer Console 개요
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822193"
---
# <span data-ttu-id="99162-103">Application Virtualization Sequencer Console 개요</span><span class="sxs-lookup"><span data-stu-id="99162-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="99162-104">App-v (Application Virtualization) Sequencer는 가상 응용 프로그램으로 가상 환경에서 실행할 수 있도록 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99162-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="99162-105">응용 프로그램이 시퀀싱 된 후에는 스트리밍 이라는 프로세스를 사용 하 여 app-v 데스크톱 클라이언트를 실행 하는 컴퓨터 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="99162-106">App-v Sequencer는 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고, 가상 환경에서 응용 프로그램을 실행 하는 데 필요한 모든 정보를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="99162-107">또한이 프로세스는 모든 사용자에 게 적용 되는 파일 및 구성 및 사용자가 사용자 지정할 수 있는 구성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="99162-108">가상 응용 프로그램은 대상 컴퓨터에서 실행 되며 대상 컴퓨터 또는 대상 컴퓨터에 설치 된 응용 프로그램에서 실행 되는 운영 체제에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="99162-109">Application Virtualization Sequencer 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="99162-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="99162-110">App-v Sequencer는 로컬 시스템 계정을 사용 하 여 시퀀싱 시간에 검색 된 모든 서비스를 실행 하 고 서비스 제어 요청에 보안 설명자를 적용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="99162-111">다른 사용자 계정을 사용 하 여 서비스를 설치 했거나 보안 설명자가 다른 사용자 그룹 특정 서비스 권한을 부여 하려는 경우 서비스를 가상화 해야 하는지 신중히 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="99162-112">의도 하지 않은 서비스 보안이 유지 되도록 서비스를 로컬로 설치 해야 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="99162-113">Application Virtualization Sequencer 콘솔 메뉴 옵션</span><span class="sxs-lookup"><span data-stu-id="99162-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="99162-114">App-v Sequencer 콘솔에서 사용할 수 있는 메뉴 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="99162-115">**파일**— 시퀀싱 된 응용 프로그램을 만들고, 열고, 수정 하 고, 저장 하는 데 도움이 되는 다양 한 명령이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="99162-116">**편집**— 기존 가상 응용 프로그램을 편집 하기 위한 다양 한 명령을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="99162-117">**보기**-가상 응용 프로그램의 속성을 보기 위한 다양 한 명령이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="99162-118">**도구**-가상 응용 프로그램을 구성 하기 위한 다양 한 도구와 진단을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="99162-119">Application Virtualization Sequencer 콘솔 도구 모음 옵션</span><span class="sxs-lookup"><span data-stu-id="99162-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="99162-120">App-v 시퀀서 콘솔에서 사용할 수 있는 도구 모음 단추는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="99162-121">**새 패키지**-클릭 하 여 새 시퀀싱 된 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99162-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="99162-122">**열기**-App-v 시퀀서 콘솔에서 시퀀싱 된 응용 프로그램 패키지를 클릭 하 여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="99162-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="99162-123">**업그레이드를 위해 열기**— 시퀀싱 된 응용 프로그램을 열고 업데이트 하거나 적용 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="99162-124">**저장**-시퀀싱 된 가상 응용 프로그램을 저장 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="99162-125">**시퀀싱 마법사**-시퀀싱 마법사를 열려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="99162-126">**도구**옵션 아래의 **일반** 탭에서 변경 작업을 수행 하는 경우 시퀀싱 마법사를 시작 하려면이 단추를 사용 해야 합니다  /  **Options**.</span><span class="sxs-lookup"><span data-stu-id="99162-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="99162-127">가상 응용 프로그램 탭</span><span class="sxs-lookup"><span data-stu-id="99162-127">Virtual Application Tabs</span></span>


<span data-ttu-id="99162-128">App-v Sequencer 콘솔에서 가상 응용 프로그램을 볼 때 다음 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99162-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="99162-129">**속성**-선택한 가상 응용 프로그램에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="99162-130">가상 응용 프로그램과 연결 된 **패키지 이름** 및 **설명을** 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="99162-131">**배포**-대상 컴퓨터에서 가상 응용 프로그램에 액세스 하는 방법에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="99162-132">가상 응용 프로그램 배달 방법을 구성할 수 있으며 대상 컴퓨터에서 실행 해야 하는 운영 체제를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="99162-133">연결 된 출력 옵션을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-133">You can also configure the associated output options.</span></span> <span data-ttu-id="99162-134">클라이언트가 파일의 가상 응용 프로그램에 액세스 하도록 하려는 경우 경로를 지정할 때 다음과 같은 형식을 사용 합니다. **File://server/share/path/.sft**.</span><span class="sxs-lookup"><span data-stu-id="99162-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="99162-135">업그레이드 중에 패키지와 연결 된 보안을 유지 하려면 **보안 설명자 적용** 을 선택 하 고, 업그레이드 중에는 해당 권한이 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99162-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="99162-136">**변경 내용**-가상 응용 프로그램에 대해 발생 한 업데이트에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="99162-137">**파일**— 선택한 가상 응용 프로그램과 연결 된 파일을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="99162-138">적절 한 필드를 사용 하 여 관련 파일 속성을 약간만 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="99162-139">**가상 레지스트리**-선택한 가상 응용 프로그램과 연결 된 가상 레지스트리를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="99162-140">적절 한 항목을 마우스 오른쪽 단추로 클릭 하 여 레지스트리 키를 추가 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="99162-141">**가상 파일 시스템**-선택한 가상 응용 프로그램과 연결 된 가상 파일 시스템을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="99162-142">해당 항목을 마우스 오른쪽 단추로 클릭 하 고 옵션을 선택 하 여이 탭에서 파일 시스템 항목을 추가, 삭제 또는 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="99162-143">**가상 서비스**-선택한 가상 응용 프로그램과 연결 된 서비스를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="99162-144">**Osd**-가상 응용 프로그램과 연결 된 Osd (개방형 소프트웨어 설명자)에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99162-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="99162-145">해당 항목을 마우스 오른쪽 단추로 클릭 하 고 원하는 작업을 선택 하 여 OSD 파일과 연결 된 파일을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99162-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="99162-146">관련 항목</span><span class="sxs-lookup"><span data-stu-id="99162-146">Related topics</span></span>


[<span data-ttu-id="99162-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="99162-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





