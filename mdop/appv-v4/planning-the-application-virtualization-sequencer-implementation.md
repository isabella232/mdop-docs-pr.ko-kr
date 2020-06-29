---
title: Application Virtualization Sequencer 구현 계획
description: Application Virtualization Sequencer 구현 계획
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815893"
---
# <span data-ttu-id="ffc70-103">Application Virtualization Sequencer 구현 계획</span><span class="sxs-lookup"><span data-stu-id="ffc70-103">Planning the Application Virtualization Sequencer Implementation</span></span>


<span data-ttu-id="ffc70-104">응용 프로그램 가상화에서 가상 응용 프로그램 및 응용 프로그램 패키지를 만드는 데 사용 되는 시퀀싱을 통해 응용 프로그램 가상화 시퀀서 소프트웨어가 설치 된 컴퓨터를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-104">Sequencing, the process used by Application Virtualization to create virtual applications and application packages, requires the use of a computer with the Application Virtualization Sequencer software installed.</span></span>

<span data-ttu-id="ffc70-105">시퀀싱 프로세스 중에 시퀀서는 모니터 모드에 배치 되 고 시퀀싱 될 응용 프로그램이 시퀀싱 컴퓨터에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-105">During the sequencing process, the Sequencer is placed in monitor mode, and the application to be sequenced is installed on the sequencing computer.</span></span> <span data-ttu-id="ffc70-106">그 다음에는 시퀀싱 된 응용 프로그램이 시작 되 고, 모니터링 프로세스에서 응용 프로그램을 실행 하는 데 필요한 응용 프로그램 패키지의 최소 콘텐츠를 포함 하는 기본 기능 블록을 구성할 수 있도록 하는 것이 가장 중요 하 고 일반적으로 사용 되는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-106">Next, the sequenced application is started, and its most important and commonly used functions are exercised so that the monitoring process can configure the primary feature block, which contains the minimum content in an application package that is necessary for an application to run.</span></span> <span data-ttu-id="ffc70-107">이러한 단계를 완료 하면 모니터링 모드가 중지 되 고 시퀀싱 된 응용 프로그램이 올바르게 작동 하는지 확인 하기 위해 저장 및 테스트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-107">When these steps are complete, monitoring mode is stopped and the sequenced application is saved and tested to verify correct operation.</span></span>

<span data-ttu-id="ffc70-108">시퀀싱을 위해 선택할 응용 프로그램을 결정할 때는 특정 응용 프로그램을 시퀀싱 할 수 없다는 점에 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-108">When deciding which applications to choose for sequencing, remember that certain applications cannot be sequenced.</span></span> <span data-ttu-id="ffc70-109">여기에는 Internet Explorer, 장치 드라이버, 부팅 시 서비스를 시작 하는 응용 프로그램 등 Windows 운영 체제의 특정 부분이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-109">These include certain parts of the Windows operating system, such as Internet Explorer, device drivers, and applications that start services at boot time.</span></span>

<span data-ttu-id="ffc70-110">Sequencer 설치에 대 한 단계별 정보는 [Application Virtualization Sequencer를 설치 하는 방법을](how-to-install-the-application-virtualization-sequencer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffc70-110">For step-by-step information about installing the Sequencer, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span>

<span data-ttu-id="ffc70-111">**중요**  전체 시퀀싱 프로세스 계획을 검토 하 고 회사 보안 팀이 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-111">**Important** The entire sequencing process plan should be reviewed and approved by your corporate security team.</span></span> <span data-ttu-id="ffc70-112">시퀀서 작업은 일반적으로 랩에서 프로덕션 환경과 별도로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-112">Sequencer operations would usually be kept separate from the production environment in a lab.</span></span> <span data-ttu-id="ffc70-113">비즈니스 요구 사항에 따라 단순 하거나 필요한 경우 포괄적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-113">This can be as simple or as comprehensive as necessary, based on your business requirements.</span></span> <span data-ttu-id="ffc70-114">시퀀싱 컴퓨터는 완료 된 패키지를 프로덕션 서버로 복사 하기 위해 회사 네트워크에 대 한 연결을 필요로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-114">The sequencing computers will need connectivity to the corporate network to copy finished packages over to the production servers.</span></span> <span data-ttu-id="ffc70-115">그러나 일반적으로 바이러스 백신 보호 없이 작동 하기 때문에 회사 네트워크에 보호 되지 않는 것이 좋습니다 (예: 방화벽이 나 격리 된 네트워크 세그먼트 뒤에서 작동할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="ffc70-115">However, because they are typically operated without antivirus protection, they must not be on the corporate network unprotected—for example, you might be able to operate behind a firewall or on an isolated network segment.</span></span> <span data-ttu-id="ffc70-116">격리 된 가상 네트워크를 공유 하도록 구성 되는 가상 컴퓨터를 사용 하는 것도 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-116">Using Virtual Machines configured to share an isolated virtual network might also be an acceptable approach.</span></span> <span data-ttu-id="ffc70-117">회사 보안 정책에 따라이 문제를 안전 하 게 해결 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffc70-117">Follow your corporate security policies to safely address this situation.</span></span>

 

<span data-ttu-id="ffc70-118">시퀀싱 프로세스를 계획 하는 주요 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-118">Key steps for planning the sequencing process include the following:</span></span>

-   <span data-ttu-id="ffc70-119">각 월을 처리 하는 데 예상 되는 응용 프로그램 수, 해당 응용 프로그램의 크기, 향후 업데이트 시퀀싱을 위한 여유를 추가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-119">Consider the number of applications you expect to process each month, the size of those applications, and add an allowance for sequencing future updates.</span></span> <span data-ttu-id="ffc70-120">패키지의 크기, 압축 또는 압축이 최대 4gb까지 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-120">Packages can be up to 4 GB in size, compressed or uncompressed.</span></span>

-   <span data-ttu-id="ffc70-121">각 응용 프로그램을 시퀀싱 할 때 조직이 수행할 체계적이 고 반복 가능한 프로세스를 준비 하 고 문서화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-121">Prepare and document a methodical, repeatable process for your organization to follow when sequencing each application.</span></span> <span data-ttu-id="ffc70-122">여기에는 각 실행에 대 한 검사 목록 및 버전 제어 프로세스의 사용이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-122">This should include the use of a checklist for each run, as well as a version control process.</span></span> <span data-ttu-id="ffc70-123">각 시퀀싱 된 응용 프로그램에 추적 로그를 사용 하는 것은 패키지에서 발생할 수 있는 기술적 문제를 조사할 때에도 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-123">The use of a tracking log for each sequenced application is also very helpful when investigating possible technical issues with a package.</span></span>

-   <span data-ttu-id="ffc70-124">응용 프로그램 시퀀싱을 위해서는 최소 4gb RAM과 고속 CPU (3 GHz 이상)를 사용 하 여 처리량을 최적화 하는 높은 성능의 컴퓨터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-124">For sequencing applications, use high-performing computers that are optimized for processing throughput, with at least 4 GB of RAM and a fast CPU (3 GHz or faster).</span></span> <span data-ttu-id="ffc70-125">빠른 하드 디스크와 별도의 디스크 볼륨을 사용 하는 경우에도 성능이 향상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-125">Fast hard disks and the use of separate disk volumes can also improve performance.</span></span> <span data-ttu-id="ffc70-126">가상 컴퓨터는 쉽게 다시 설정할 수 있기 때문에 시퀀싱 하는 데 적합 하거나, 각 패키지 시퀀싱 작업이 완료 된 후 빠른 다시 이미징을 사용할 수 있도록 로컬 파티션에 깨끗 한 이미지가 있는 물리적 컴퓨터를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-126">Virtual Machines are ideal for sequencing because they can easily be reset, or you can use a physical computer with a clean image on a local partition to enable rapid re-imaging after each package sequencing operation has been completed.</span></span>

    <span data-ttu-id="ffc70-127">**중요**  안전 모드에서 App-v 시퀀서를 실행 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-127">**Important** Running the App-V sequencer in Safe Mode is not supported.</span></span>

     

-   <span data-ttu-id="ffc70-128">응용 프로그램을 시퀀싱 하기 전에 시퀀싱 컴퓨터에 설치 해야 하는지 여부를 결정 하는 경우가 많으므로 Microsoft Office 또는 Java 런타임 환경과 같은 통합 요소를 포함 하 여 시퀀싱 된 응용 프로그램의 운영 환경을 이해 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-128">Verify that you understand the sequenced application’s operating environment, including integration elements such as Microsoft Office or the Java Runtime Environment, because this will often determine whether anything has to be installed on the sequencing computer prior to sequencing the application.</span></span>

-   <span data-ttu-id="ffc70-129">각각의 새 시퀀싱 작업이 항상 깨끗 한 기본 이미지로 시작 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-129">Ensure that each new sequencing operation always starts with a clean base image.</span></span> <span data-ttu-id="ffc70-130">저장 된 이미지를 물리적 컴퓨터로 복원 하거나 변경 내용을 모두 취소 한 후 가상 컴퓨터를 다시 시작 하 여 시퀀싱 하는 컴퓨터가 다시 설정 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-130">Make sure that the sequencing computer has been reset, either by restoring the saved image to a physical computer or by restarting a virtual machine after discarding all changes.</span></span> <span data-ttu-id="ffc70-131">기본 이미지는 저장 하기 전에 Windows 업데이트에서 적용 된 최신 업데이트를 보유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-131">The base image should have the latest updates applied from Windows Update before saving.</span></span>

-   <span data-ttu-id="ffc70-132">시퀀싱 프로세스 중에 안정적인 플랫폼을 사용 하는 것이 중요 하기 때문에 설치 모니터링 프로세스 (예: 바이러스 검사 프로그램 및 Windows 업데이트)를 방해할 수 있는 시퀀싱 컴퓨터에서 모두 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-132">Turn off anything on the sequencing computer that can interfere with the install monitoring process, such antivirus scanners and Windows Update, because having a stable platform during the sequencing process is essential.</span></span> <span data-ttu-id="ffc70-133">이 단계는 심각한 보안 위험을 발생 하기 때문에, 시퀀싱 된 응용 프로그램 패키지를 비롯 하 여 컴퓨터와 네트워크를 보호 하기 위해 올바른 예방 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-133">Because this step incurs significant security risks, ensure that the correct precautions are taken to protect the computer and network as well as the sequenced application package.</span></span> <span data-ttu-id="ffc70-134">시퀀싱 하기 전에 응용 프로그램 패키지의 바이러스 백신 검사를 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-134">We recommend that you do an antivirus scan of application packages before sequencing them.</span></span>

-   <span data-ttu-id="ffc70-135">시퀀싱 후 각 응용 프로그램을 테스트 하기 위한 세부적인 프로세스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-135">Include a detailed process for testing each application after sequencing.</span></span> <span data-ttu-id="ffc70-136">시퀀싱 된 응용 프로그램을 테스트 하면 가상화 된 응용 프로그램을 최종 사용자에 게 배포 하기 전에 프로세스가 제대로 작동 하 고 프로세스의 필수 요소 인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-136">Testing the sequenced application will determine whether it functions correctly and is an essential part of the process prior to deploying the virtualized application to end users.</span></span> <span data-ttu-id="ffc70-137">대규모 배포 전에 최종 사용자에 대 한 테스트의 마지막 단계로 테스트 그룹에 대 한 파일럿 배포도 계획 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-137">As the final step in testing prior to wide-scale deployment to end users, you should also plan for a pilot deployment to a test group.</span></span>

-   <span data-ttu-id="ffc70-138">시퀀싱 된 응용 프로그램을 테스트 하는 경우 동일한 형식의 컴퓨터 장비를 선택 하 고 회사 프로덕션 환경에서 사용 중인 운영 체제와 동일한 시스템을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-138">When testing sequenced applications, choose computer equipment of the same type and running the same operating systems that are in use in the company production environment.</span></span> <span data-ttu-id="ffc70-139">올바르게 구성 되어 있으면 가상 컴퓨터 또는 물리적 컴퓨터 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc70-139">As long as they are configured properly, either virtual machines or physical machines can be used.</span></span>

## <span data-ttu-id="ffc70-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ffc70-140">Related topics</span></span>


[<span data-ttu-id="ffc70-141">Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="ffc70-141">Application Virtualization Sequencer Hardware and Software Requirements</span></span>](application-virtualization-sequencer-hardware-and-software-requirements.md)

[<span data-ttu-id="ffc70-142">Application Virtualization Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="ffc70-142">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="ffc70-143">Application Virtualization Sequencer 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="ffc70-143">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="ffc70-144">보안 및 보호 개요</span><span class="sxs-lookup"><span data-stu-id="ffc70-144">Security and Protection Overview</span></span>](security-and-protection-overview.md)

 

 





