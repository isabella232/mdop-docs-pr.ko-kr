---
title: OSD 파일 요소
description: OSD 파일 요소
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816108"
---
# <span data-ttu-id="2ad1e-103">OSD 파일 요소</span><span class="sxs-lookup"><span data-stu-id="2ad1e-103">OSD File Elements</span></span>


<span data-ttu-id="2ad1e-104">Sequencer 설치 디렉터리에는 OSD (개방형 소프트웨어 설명자) 파일의 유효한 구조를 정의 하는 XML 스키마 파일인 **Softricity**이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="2ad1e-105">다음은 자주 사용 하는 OSD 요소 중 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="2ad1e-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="2ad1e-106">SOFTPKG</span></span>  
<span data-ttu-id="2ad1e-107">소프트웨어 패키지를 정의 하는 모든 요소가 포함 된 OSD 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="2ad1e-108">CODEBASE</span><span class="sxs-lookup"><span data-stu-id="2ad1e-108">CODEBASE</span></span>  
<span data-ttu-id="2ad1e-109">이 패키지의 sft 파일에 대 한 정보 (HREF, FILENAME, GUID 특성 포함)입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="2ad1e-110">이 특정 패키지의 배포 지점을 변경 하는 경우 HREF 특성을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="2ad1e-111">OS</span><span class="sxs-lookup"><span data-stu-id="2ad1e-111">OS</span></span>  
<span data-ttu-id="2ad1e-112">시퀀싱 마법사에서 초기에 설정 된 값을 기준으로이 응용 프로그램을 실행할 수 있는 운영 체제를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="2ad1e-113">이 값에는 **Softricity**에 정의 된 값만 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="2ad1e-114">지역 \ _INTERACTION \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="2ad1e-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="2ad1e-115">TRUE로 설정 하면 특정 가상 환경 내에서 격리 되지 않고 전역 네임 스페이스의 명명 된 개체 (이벤트, 뮤텍스, 세마포, 파일 매핑 및 mailslots) 및 COM 개체를 만들 수 있으며,이는 가상 응용 프로그램이 호스트 운영 체제의 응용 프로그램과 상호 작용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="2ad1e-116">예: &lt; SOFTPKG &gt; &lt; 구현&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="2ad1e-117">&lt;VIRTUALENV &gt; &lt; 정책&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="2ad1e-118">&lt;로컬 \ _INTERACTION \ _ALLOWED &gt; TRUE</span><span class="sxs-lookup"><span data-stu-id="2ad1e-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="2ad1e-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="2ad1e-120">&lt;/REE &gt; &lt; /정책/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="2ad1e-121">&lt;/구현 &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="2ad1e-122">항목</span><span class="sxs-lookup"><span data-stu-id="2ad1e-122">DEPENDENCIES</span></span>  
<span data-ttu-id="2ad1e-123">다른 패키지의 CODEBASE 태그를 사용 하 여 동적 도구 모음 컴퍼지션 (다른 패키지에 대 한 종속성)을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="2ad1e-124">예: &lt; 종속성 &gt; &lt; CODEBASE HREF = "rtsps:/server/package.sft" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "installer.pkg" "SIZE =" osguard "필수 =" FALSE "/ &gt; &lt; /종속성&gt;</span><span class="sxs-lookup"><span data-stu-id="2ad1e-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="2ad1e-125">패키지 이름</span><span class="sxs-lookup"><span data-stu-id="2ad1e-125">PACKAGE NAME</span></span>  
<span data-ttu-id="2ad1e-126">시퀀싱 마법사 **패키지 정보** 페이지에 입력 한 패키지의 일반 이름으로, 여러 응용 프로그램을 포함 하는 시퀀싱 된 응용 프로그램에 사용 되는 단일 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="2ad1e-127">타이틀이</span><span class="sxs-lookup"><span data-stu-id="2ad1e-127">TITLE</span></span>  
<span data-ttu-id="2ad1e-128">시퀀싱 하는 응용 프로그램의 선택적 설명적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="2ad1e-129">이론적인</span><span class="sxs-lookup"><span data-stu-id="2ad1e-129">ABSTRACT</span></span>  
<span data-ttu-id="2ad1e-130">시퀀싱 마법사 **패키지 정보** 페이지의 **설명** 필드에 입력 된 소프트웨어 패키지에 대 한 간략 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="2ad1e-131">모범 사례는 운영 체제 및 Sequencer workstation 서비스 팩 수준, Sequencer 버전, 시퀀싱 엔지니어의 이름 등의 정보를 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="2ad1e-132">스크립팅할</span><span class="sxs-lookup"><span data-stu-id="2ad1e-132">SCRIPT</span></span>  
<span data-ttu-id="2ad1e-133">시작, 종료 또는 스트리밍 중 발생할 특정 스크립팅된 이벤트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="2ad1e-134">관리 \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="2ad1e-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="2ad1e-135">마법사에 정의 된 모든 바로 가기 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="2ad1e-136">관리 \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="2ad1e-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="2ad1e-137">마법사에 지정 된 파일 형식 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad1e-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="2ad1e-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ad1e-138">Related topics</span></span>


[<span data-ttu-id="2ad1e-139">OSD 탭 정보</span><span class="sxs-lookup"><span data-stu-id="2ad1e-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





