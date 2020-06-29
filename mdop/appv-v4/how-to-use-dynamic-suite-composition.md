---
title: Dynamic Suite Composition을 사용하는 방법
description: Dynamic Suite Composition을 사용하는 방법
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816418"
---
# <span data-ttu-id="9e094-103">Dynamic Suite Composition을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="9e094-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="9e094-104">Application Virtualization의 동적 도구 모음 컴퍼지션은 응용 프로그램을 미들웨어 또는 플러그 인과 같은 다른 응용 프로그램에 종속 되는 것으로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="9e094-105">이렇게 하면 응용 프로그램에서 가상 환경의 미들웨어 또는 플러그 인과 상호 작용할 수 있으며,이 경우 일반적으로이는 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="9e094-106">이는 보조 응용 프로그램 패키지를 *기본 응용*프로그램 이라고 하는 여러 다른 응용 프로그램에서 사용할 수 있기 때문에, 각 기본 응용 프로그램이 동일한 보조 패키지를 참조할 수 있도록 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="9e094-107">ActiveX 컨트롤 등의 플러그 인에 의존 하는 응용 프로그램을 시퀀싱 하거나 OLE DB 또는 JRE (Java 런타임 환경) 등의 미들웨어를 사용 하는 경우 동적 도구 모음 컴퍼지션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="9e094-108">이러한 종속 구성 요소를 사용 하는 각 응용 프로그램에 구성 요소를 포함 하 여 시퀀싱 해야 하는 경우 이러한 구성 요소에 대 한 업데이트는 모든 기본 응용 프로그램을 다시 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="9e094-109">구성 요소 없이 기본 응용 프로그램을 시퀀싱 한 다음 미들웨어 또는 플러그 인을 보조 패키지로 시퀀싱 하는 경우 보조 패키지만 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="9e094-110">이 방법의 한 가지 장점은 기본 패키지의 크기를 줄이는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="9e094-111">또 다른 이점은 보조 응용 프로그램에 대 한 액세스 권한을 더 효과적으로 제어할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="9e094-112">보조 응용 프로그램은 일반적인 방식으로 스트리밍할 수 있으며, 실행 하기 위해 완전히 캐시 되지 않아도 된다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e094-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="9e094-113">기본 패키지는 두 개 이상의 보조 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="9e094-114">그러나 한 수준의 종속성만 지원 되므로 보조 패키지를 다른 보조 패키지에 종속 되는 것으로 정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="9e094-115">또한 보조 응용 프로그램은 미들웨어 또는 플러그인만 가능 하며 다른 완전 한 소프트웨어 제품 일 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="9e094-116">여러 기본 응용 프로그램이 단일 미들웨어 제품에 종속 되 게 하려면 배포 하기 전에이 구성을 테스트 하 여 시스템 성능에 미칠 수 있는 영향을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="9e094-117">**중요**  패키지 종속성은 기본 응용 프로그램에 대해 필수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="9e094-118">보조 패키지가 필수로 플래그가 지정 되 고 로드 중 몇 가지 이유로 액세스할 수 없는 경우에는 보조 패키지의 로드가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="9e094-119">또한 기본 응용 프로그램은 사용자가 시작 하려고 할 때 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="9e094-120">다음 절차를 사용 하 여 플러그 인 또는 미들웨어 구성 요소에 대 한 보조 패키지를 만든 다음 마지막 절차를 사용 하 여 보조 패키지의 OSD 파일에서 종속성을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="9e094-121">동적 도구 모음 컴퍼지션을 사용 하 여 플러그 인에 대 한 보조 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="9e094-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="9e094-122">깨끗 한 이미지로 설정 된 시퀀싱 컴퓨터에서 Application Virtualization Sequencer를 설치 하 고 컴퓨터 상태를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="9e094-123">기본 응용 프로그램을 시퀀싱 하 고 패키지를 서버의 콘텐츠 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="9e094-124">1 단계의 저장 된 상태로 시퀀싱 컴퓨터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="9e094-125">기본 응용 프로그램을 시퀀싱 컴퓨터에 로컬로 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="9e094-126">**중요**  보조 패키지에 대 한 새 패키지 루트를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="9e094-127">시퀀서 모니터링 단계를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="9e094-128">시퀀싱 컴퓨터에 플러그 인을 설치 하 고 필요에 따라 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="9e094-129">기본 응용 프로그램을 열고 플러그 인이 제대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="9e094-130">Sequencer 콘솔에서 플러그 인을 포함 하는 보조 패키지를 나타내고 아이콘을 선택 하는 더미 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="9e094-131">패키지를 서버의 Content 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="9e094-132">**참고**  보조 패키지 관리를 지원 하기 위해 패키지 이름에는 독립 실행형 응용 프로그램 역할을 하는 패키지 라는 것을 강조 하기 위해 "보조 패키지" 라는 용어를 포함 하는 것이 좋습니다 (예: **\ [name-plug-ins \] 보조 패키지**).</span><span class="sxs-lookup"><span data-stu-id="9e094-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="9e094-133">동적 도구 모음 컴퍼지션을 사용 하 여 미들웨어에 대 한 보조 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="9e094-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="9e094-134">깨끗 한 이미지로 설정 된 시퀀싱 컴퓨터에서 Application Virtualization Sequencer를 설치 하 고 컴퓨터 상태를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="9e094-135">시퀀싱 하는 컴퓨터에 미들웨어를 로컬로 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="9e094-136">기본 응용 프로그램을 시퀀싱 하 고 패키지를 서버의 콘텐츠 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="9e094-137">1 단계의 저장 된 상태로 시퀀싱 컴퓨터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="9e094-138">Sequencer를 시작 하 여 새 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="9e094-139">시퀀서 모니터링 단계를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="9e094-140">시퀀싱 하는 컴퓨터에 미들웨어 응용 프로그램을 설치 하 고 일반 설치와 같이 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="9e094-141">시퀀싱 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="9e094-142">패키지를 서버의 Content 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="9e094-143">**참고**  보조 패키지 관리를 지원 하려면 패키지 이름에 "보조 패키지" 라는 용어를 포함 하 여 독립 실행형 응용 프로그램 역할을 하는 패키지 라는 것을 강조 합니다 (예: **\ [미들웨어 name \] 보조 패키지**).</span><span class="sxs-lookup"><span data-stu-id="9e094-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="9e094-144">기본 패키지에서 종속성을 정의 하려면</span><span class="sxs-lookup"><span data-stu-id="9e094-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="9e094-145">서버에서 편집을 위해 보조 패키지의 OSD 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="9e094-146">(XML 편집기를 사용 하 여 OSD 파일을 변경 하는 것이 좋습니다. 하지만 다른 방법으로는 메모장을 사용할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="9e094-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="9e094-147">해당 파일의 **CODEBASE HREF** 줄을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="9e094-148">편집을 위해 기본 패키지의 OSD 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="9e094-149"><strong> &lt; &gt; </strong> \*\* &lt; Virtualenv &gt; \*\* 섹션의 끝에 있는 \*\* &lt; /ENVLIST &gt; \*\* 태그 뒤에 \*\* &lt; /tvirtualenv &gt; \*\* 태그 바로 앞에 있는 종속성 태그를 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="9e094-150">방금 만든 \*\* &lt; 종속성 &gt; \*\* 태그 뒤에 보조 패키지의 **CODEBASE HREF** 줄을 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="9e094-151">보조 패키지가 필수 패키지 인 경우 기본 패키지를 시작 하기 전에 시작 해야 하는 경우 **CODEBASE** 태그 내에 **필수 = "TRUE"** 속성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="9e094-152">필수 항목이 아니면 속성을 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="9e094-153">\*\* &lt; 종속성 &gt; \*\* 태그를 닫으려면 다음을 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="9e094-154">&lt;/종속성&gt;</span><span class="sxs-lookup"><span data-stu-id="9e094-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="9e094-155">OSD 파일에 대 한 변경 내용을 검토 한 다음 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="9e094-156">다음 예제에서는 추가 된 섹션을 표시 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="9e094-157">예를 들어 여기에 표시 된 태그 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="9e094-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="9e094-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="9e094-159">…</span><span class="sxs-lookup"><span data-stu-id="9e094-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="9e094-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="9e094-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="9e094-161">보조 패키지에 OSD 파일의 \*\* &lt; ENVLIST &gt; \*\* 섹션에 있는 항목이 있는 경우 해당 항목을 기본 패키지의 동일한 섹션으로 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e094-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="9e094-162">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9e094-162">Related topics</span></span>


[<span data-ttu-id="9e094-163">앱-V 시퀀서를 사용 하 여 가상 응용 프로그램을 만들거나 업그레이드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9e094-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





