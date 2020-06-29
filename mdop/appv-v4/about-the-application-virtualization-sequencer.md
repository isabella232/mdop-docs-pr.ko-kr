---
title: Application Virtualization Sequencer 정보
description: Application Virtualization Sequencer 정보
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819998"
---
# <span data-ttu-id="5b924-103">Application Virtualization Sequencer 정보</span><span class="sxs-lookup"><span data-stu-id="5b924-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="5b924-104">Microsoft App-v (Application Virtualization) Sequencer는 응용 프로그램의 모든 설치 및 설정 프로세스를 모니터링 하 고 기록 하 고, **.ico**, **OSD**, **SFT**, **SPRJ**파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="5b924-105">이러한 파일에는 응용 프로그램에 대 한 모든 필수 정보가 포함 되어 있으므로 대상 컴퓨터의 가상 환경에서 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="5b924-106">Microsoft Application Virtualization (App-v) Sequencer를 사용 하 여 가상 응용 프로그램을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="5b924-107">응용 프로그램을 시퀀싱 한 후 대상 컴퓨터로 스트리밍할 수 있으며 가상 응용 프로그램 패키지의 콘텐츠를 다운로드 하 고 응용 프로그램을 로컬로 실행 하 여 대상 컴퓨터에서 가상 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="5b924-108">**중요**  가상 응용 프로그램 패키지를 실행 하려면 대상 컴퓨터가 App-v 클라이언트의 적절 한 버전을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="5b924-109">가상 응용 프로그램 패키지는 각 응용 프로그램이 가상 환경에서 실행 되 고 대상 컴퓨터에 설치 되거나 실행 되는 다른 응용 프로그램과 격리 되므로 대상 컴퓨터의 기본 운영 체제와 상호 작용 하지 않고 대상 컴퓨터에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="5b924-110">이러한 격리는 응용 프로그램 충돌을 줄일 수 있으며 필요한 응용 프로그램 사전 배포 테스트의 양을 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="5b924-111">Sequencer 용어</span><span class="sxs-lookup"><span data-stu-id="5b924-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="5b924-112">Application Virtualization 드라이브</span><span class="sxs-lookup"><span data-stu-id="5b924-112">Application Virtualization drive</span></span>  
<span data-ttu-id="5b924-113">응용 프로그램 가상화 드라이브는 시퀀싱 된 응용 프로그램이 실행 되는 대상 컴퓨터의 기본 드라이브 (Q:\)입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="5b924-114">.ICO 파일</span><span class="sxs-lookup"><span data-stu-id="5b924-114">ICO file</span></span>  
<span data-ttu-id="5b924-115">시퀀싱 된 응용 프로그램을 시작 하는 데 사용 되는 클라이언트 데스크톱의 아이콘 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="5b924-116">설치 디렉터리</span><span class="sxs-lookup"><span data-stu-id="5b924-116">Installation directory</span></span>  
<span data-ttu-id="5b924-117">설치 하는 동안 sequencer에서 설치 파일을 배치 하는 데 사용 되는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="5b924-118">OSD (개방형 소프트웨어 설명자) 파일</span><span class="sxs-lookup"><span data-stu-id="5b924-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="5b924-119">App-v 클라이언트에 app-v 스트리밍 서버에서 시퀀싱 된 응용 프로그램을 검색 하는 방법과 가상 환경에서 시퀀싱 된 응용 프로그램을 실행 하는 방법에 대해 설명 하는 XML 기반 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="5b924-120">패키지 루트 디렉터리</span><span class="sxs-lookup"><span data-stu-id="5b924-120">Package root directory</span></span>  
<span data-ttu-id="5b924-121">시퀀싱 한 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지의 파일이 설치 된 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="5b924-122">이 디렉터리는 시퀀싱 된 응용 프로그램이 스트리밍되는 컴퓨터에도 사실상 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="5b924-123">시퀀싱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="5b924-123">Sequenced application</span></span>  
<span data-ttu-id="5b924-124">시퀀서에서 모니터링 하는 응용 프로그램을 기본 및 보조 기능 블록으로 분할 하 고, App-v 클라이언트 t를 실행 하는 대상 컴퓨터로 스트리밍 하 고, 가상 환경을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="5b924-125">시퀀싱 되는 응용 프로그램 패키지</span><span class="sxs-lookup"><span data-stu-id="5b924-125">Sequenced application package</span></span>  
<span data-ttu-id="5b924-126">가상 응용 프로그램을 구성 하 고 가상 응용 프로그램을 실행할 수 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="5b924-127">이러한 파일은 시퀀싱, **sft**, **sprj**, **.ico** 파일을 순서 **대로 포함 하**여 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="5b924-128">시퀀스</span><span class="sxs-lookup"><span data-stu-id="5b924-128">Sequencing</span></span>  
<span data-ttu-id="5b924-129">App-v 시퀀서를 사용 하 여 응용 프로그램 패키지를 만드는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="5b924-130">이 프로세스에서는 응용 프로그램이 모니터링 되 고 해당 바로 가기가 구성 되며 시퀀싱 된 응용 프로그램 패키지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="5b924-131">시퀀싱 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="5b924-131">Sequencing computer</span></span>  
<span data-ttu-id="5b924-132">응용 프로그램을 시퀀싱 하는 데 사용 되는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="5b924-133">가상 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="5b924-133">Virtual application</span></span>  
<span data-ttu-id="5b924-134">시퀀서에 의해 패키지 된 응용 프로그램을 자체 포함 가상 환경에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="5b924-135">가상 환경에는 응용 프로그램을 로컬로 설치 하지 않고 클라이언트에서 응용 프로그램을 실행 하는 데 필요한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="5b924-136">기본 기능 블록</span><span class="sxs-lookup"><span data-stu-id="5b924-136">Primary feature block</span></span>  
<span data-ttu-id="5b924-137">대상 컴퓨터에서 응용 프로그램을 실행 하는 데 필요한 가상 응용 프로그램 패키지의 최소 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="5b924-138">기본 기능 블록의 콘텐츠는 시퀀싱 하는 응용 프로그램 단계에서 식별 되며 일반적으로 사용 되는 응용 프로그램 기능에 대 한 콘텐츠로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="5b924-139">시퀀싱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="5b924-139">Sequencing Applications</span></span>


<span data-ttu-id="5b924-140">환경에서 가상 응용 프로그램 패키지를 만들고 수정 하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="5b924-141">첫 번째 방법은 **시퀀싱** 마법사를 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="5b924-142">**시퀀싱** 마법사를 사용 하 여 새로 만들거나 기존 가상 응용 프로그램 패키지를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="5b924-143">**시퀀싱** 마법사를 사용 하는 방법에 대 한 자세한 내용은 [새 응용 프로그램을 시퀀싱 하는 방법](how-to-sequence-a-new-application.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b924-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="5b924-144">두 번째 방법은 명령줄을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-144">The second method is by using the command-line.</span></span> <span data-ttu-id="5b924-145">명령줄에서 명령 프롬프트를 사용 하 여 새를 만들거나 기존 가상 응용 프로그램 패키지를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="5b924-146">명령줄을 사용 하는 방법에 대 한 자세한 내용은 [명령줄을 사용 하 여 가상 응용 프로그램을 관리 하는 방법](how-to-manage-virtual-applications-using-the-command-line.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b924-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="5b924-147">**시퀀싱** 마법사는 가상 응용 프로그램 패키지를 만들기 위해 다음과 같은 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="5b924-148">**패키지 구성**: **시퀀싱** 마법사는 시퀀싱 된 응용 프로그램 패키지를 시작 하는 데 필요한 파일인 OSD (Open Software Descriptor) 파일을 완료 하는 데 필요한 패키지 구성 정보에 대 한 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="5b924-149">**응용 프로그램 설치**: **시퀀싱** 마법사는 응용 프로그램의 설치 및 시작 구성에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="5b924-150">이 프로그램은 응용 프로그램과 관련 된 설치 및 시작 정보를 모니터링 하 고 기록 하 여 가상 응용 프로그램 패키지에 필요한 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="5b924-151">**응용 프로그램 시작**: **시퀀싱** 마법사는 대상 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지의 초기 시작을 수행 하는 데 필요한 코드 블록을 컴파일하고 정렬 하기 위한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="5b924-152">코드 블록의 컴파일은 기본 기능 블록 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="5b924-153">Application Virtualization Sequencer 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="5b924-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="5b924-154">App-v Sequencer는 로컬 시스템 계정을 사용 하 여 시퀀싱 시간에 검색 된 모든 서비스를 실행 하 고 서비스 제어 요청에 보안 설명자를 적용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="5b924-155">다른 사용자 계정을 사용 하 여 서비스를 설치 했거나 보안 설명자가 다른 사용자 그룹 특정 서비스 권한을 부여 하려는 경우 서비스를 가상화 해야 하는지 신중히 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="5b924-156">의도 하지 않은 서비스 보안이 유지 되도록 서비스를 로컬로 설치 해야 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="5b924-157">**중요**  가상 응용 프로그램 패키지는 항상 안전한 위치에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b924-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="5b924-158">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5b924-158">Related topics</span></span>


[<span data-ttu-id="5b924-159">Application Virtualization Sequencer 개요</span><span class="sxs-lookup"><span data-stu-id="5b924-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





