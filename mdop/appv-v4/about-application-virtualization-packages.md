---
title: Application Virtualization 패키지 정보
description: Application Virtualization 패키지 정보
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820083"
---
# <span data-ttu-id="e8c14-103">Application Virtualization 패키지 정보</span><span class="sxs-lookup"><span data-stu-id="e8c14-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="e8c14-104">응용 프로그램 가상화에서 *패키지* 는 시퀀싱 프로세스의 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="e8c14-105">서버에 응용 프로그램을 처음 배포할 때와 새 버전으로 응용 프로그램을 업그레이드 하는 경우 패키지를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="e8c14-106">패키지를 사용 하 여 응용 프로그램 가상화 관리 서버에서 가상 응용 프로그램 버전을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="e8c14-107">단일 패키지에는 하나 이상의 응용 프로그램이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="e8c14-108">각 응용 프로그램 패키지에는 자체 포함 단위의 파일 집합이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="e8c14-109">패키지 관리</span><span class="sxs-lookup"><span data-stu-id="e8c14-109">Managing Packages</span></span>


<span data-ttu-id="e8c14-110">Sequencer가 프로세스의 일부로 하나 이상의 응용 프로그램 패키지를 만든 후 시퀀서에서 생성 된 파일을 응용 프로그램 가상화 관리 서버에 복사 하 여 스트리밍할 수 있도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="e8c14-111">사용 가능한 패키지는 응용 프로그램 가상화 관리 콘솔의 왼쪽 창에 있는 **패키지** 컨테이너 아래에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="e8c14-112">Sequencer 프로젝트 (SPRJ) 파일이 나 OSD (개방형 소프트웨어 설명자) 파일을 사용 하 여 응용 프로그램을 가져오면 **패키지** 컨테이너에 관련 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="e8c14-113">응용 프로그램 가상화 서버 관리 콘솔에서 패키지 및 해당 버전을 배포, 업그레이드 또는 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="e8c14-114">각 가상 응용 프로그램에는 연결 된 패키지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="e8c14-115">이 패키지에는 다음 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-115">This package includes the following files:</span></span>

-   <span data-ttu-id="e8c14-116">SFT-응용 프로그램을 클라이언트로 스트리밍하는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="e8c14-117">OSD-열려 있는 소프트웨어 설명자 파일에는 응용 프로그램을 찾아 실행 하는 데 필요한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="e8c14-118">.ICO-사용자 인터페이스 및 바로 가기에서 시각적으로 응용 프로그램을 나타내는 아이콘 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="e8c14-119">SPRJ-Sequencer 프로젝트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="e8c14-120">SPRJ 파일을 가져올 때 기본적으로 모든 시퀀싱 된 응용 프로그램을 배포에 사용할 수 있지만 응용 프로그램은 스트리밍을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="e8c14-121">패키지의 일부 또는 일부 응용 프로그램을 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="e8c14-122">예를 들어 Microsoft Office를 시퀀싱 하 고 가져온 경우 사용자 설정 저장 마법사와 같은 일부 응용 프로그램을 배포 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="e8c14-123">이 경우에는 배포할 각 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **사용** 상자 (비어 있음)가 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="e8c14-124">**사용할 수** 있는 상자가 선택 된 응용 프로그램만 클라이언트 컴퓨터로 스트림 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="e8c14-125">패키지를 resequence 하 고 스트리밍을 위해 새 SFT 파일을 만든 후에는 응용 프로그램 가상화 서버 관리 콘솔을 통해 이전 패키지를 빠르고 쉽게 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="e8c14-126">**패키지 노드를** 사용 해야 하는 유일한 작동 시나리오는 패키지용 새 버전 (SFT 파일)을 도입 하는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="e8c14-127">응용 프로그램을 가져올 때마다 액세스 및 라이선스를 응용 프로그램에 할당 하면 응용 프로그램 가상화 시스템에서 패키지 수준에이 정보를 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="e8c14-128">즉, 사용자가 응용 프로그램을 사용 하도록 권한을 부여 하면 동일한 패키지에서 모든 응용 프로그램을 실행할 수 있는 권한을 사용자에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="e8c14-129">패키지 버전</span><span class="sxs-lookup"><span data-stu-id="e8c14-129">Package Version</span></span>

<span data-ttu-id="e8c14-130">패키지 버전은 특정 SFT 파일로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="e8c14-131">패키지를 업그레이드 (응용 프로그램에 업데이트 적용 또는 패키지에 응용 프로그램 추가) 하는 경우 새 SFT 파일이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="e8c14-132">새 SFT 파일을 만들 때마다 새 패키지 버전이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="e8c14-133">응용 프로그램 가상화 서버 관리 콘솔을 통해 응용 프로그램을 가져오는 경우 소프트웨어는 패키지와 패키지 버전이 아직 없는 경우 자동으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8c14-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="e8c14-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8c14-134">Related topics</span></span>


[<span data-ttu-id="e8c14-135">Application Virtualization 응용 프로그램 정보</span><span class="sxs-lookup"><span data-stu-id="e8c14-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="e8c14-136">Application Virtualization Server Management Console 정보</span><span class="sxs-lookup"><span data-stu-id="e8c14-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="e8c14-137">Server Management Console에서 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8c14-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





