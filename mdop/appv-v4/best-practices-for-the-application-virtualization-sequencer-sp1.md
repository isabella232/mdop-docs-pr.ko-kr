---
title: Application Virtualization Sequencer의 모범 사례
description: Application Virtualization Sequencer의 모범 사례
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821998"
---
# <span data-ttu-id="4b5b6-103">Application Virtualization Sequencer의 모범 사례</span><span class="sxs-lookup"><span data-stu-id="4b5b6-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="4b5b6-104">이 항목에서는 Microsoft App-v (Application Virtualization) Sequencer를 실행 하기 위한 모범 사례를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="4b5b6-105">환경에서 시퀀서를 계획 하 고 사용할 때 다음과 같은 권장 사항을 검토 하 고 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="4b5b6-106">시퀀싱 컴퓨터 구성 모범 사례</span><span class="sxs-lookup"><span data-stu-id="4b5b6-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="4b5b6-107">App-v Sequencer를 실행 하는 컴퓨터를 구성할 때 다음과 같은 모범 사례를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="4b5b6-108">비슷한 구성을 가지 며 대상 컴퓨터 보다 이전 버전의 운영 체제를 실행 하는 컴퓨터의 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="4b5b6-109">Sequencer를 실행 하는 컴퓨터가 대상 컴퓨터 보다 이전 버전의 운영 체제를 실행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="4b5b6-110">여기에는 서비스 팩 및 업데이트 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="4b5b6-111">예를 들어 대상 컴퓨터에서 WindowsVista 및 WindowsXP를 실행 하는 경우에는 WindowsXP를 실행 하는 컴퓨터에 응용 프로그램을 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="4b5b6-112">한 운영 체제에서 시퀀스를 실행 하 고 다른 운영 체제에서 가상화 된 응용 프로그램을 실행할 수 있는 기능은 보장 되지 않으며 특정 응용 프로그램 및 운영 체제에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="4b5b6-113">문제가 발생 하는 경우 App-v 클라이언트가 실행 되는 운영 체제 환경과 동일한 환경에서 순서를 설정 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="4b5b6-114">여러 파티션을 사용 하 여 시퀀서를 실행 하는 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="4b5b6-115">두 개 이상의 주 파티션을 사용 하 여 시퀀서를 실행 하는 컴퓨터를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="4b5b6-116">첫 번째 파티션 (**C:**)은 운영 체제를 포함 해야 하며, NTFS 파일 시스템을 사용 하 여 포맷 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="4b5b6-117">두 번째 파티션 (**Q:**)은 가상 응용 프로그램 설치의 대상 경로로 사용 되며 NTFS 파일 시스템을 사용 하 여 형식도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="4b5b6-118">충분 한 디스크 공간을 사용 하 여 임시 디렉터리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="4b5b6-119">시퀀서는 시퀀싱 하는 동안 임시 파일을 저장 하는 데 **% TMP%** 또는 **% TEMP%** 디렉터리 및 **스크래치** 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="4b5b6-120">Sequencer를 실행 하는 컴퓨터에서 예상 되는 응용 프로그램 설치 요구 사항에 해당 하는 디스크 공간을 사용 하 여 이러한 디렉터리를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="4b5b6-121">Sequencer 콘솔을 열고 **도구**, **옵션**을 선택한 다음 **경로** 탭을 선택 하 여 **스크래치** 디렉터리의 위치를 확인할 수 있습니다. 다른 하드 드라이브 파티션에서 임시 디렉터리 및 **스크래치** 디렉터리를 구성 하면 시퀀싱 하는 동안 성능이 향상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="4b5b6-122">Microsoft VirtualPC를 사용 하 여 응용 프로그램을 시퀀싱 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="4b5b6-123">대부분의 응용 프로그램을 두 번 이상 시퀀싱 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="4b5b6-124">이를 쉽게 수행할 수 있도록 가상 환경에서 실행 되는 컴퓨터에서 시퀀싱을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="4b5b6-125">이를 통해 응용 프로그램을 시퀀싱 하 고 시퀀서를 실행 하는 컴퓨터에서 최소 재구성을 통해 깨끗 한 상태로 되돌릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="4b5b6-126">환경에서 Microsoft Hyper-v를 실행 하는 경우 앱이 실행 되는 Hyper-v 가상 컴퓨터가 다음과 같이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="4b5b6-127">일시 중지 및 다시 시작.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-127">paused and resumed.</span></span>

    -   <span data-ttu-id="4b5b6-128">의 상태를 저장 하 고 복원 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="4b5b6-129">스냅숏으로 저장 되며 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="4b5b6-130">실시간 마이그레이션의 일부로 다른 하드웨어에 마이그레이션.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="4b5b6-131">새 응용 프로그램을 시퀀싱 하기 전에 실행 중인 다른 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="4b5b6-132">시퀀싱 컴퓨터에서 일반적으로 실행 되는 프로세스 및 예약 된 작업은 시퀀싱 프로세스의 속도를 늦추거나 시퀀싱 중에 관련이 없는 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="4b5b6-133">시퀀싱을 시작 하기 전에 불필요 한 모든 응용 프로그램과 프로그램을 종료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="4b5b6-134">터미널 서비스를 실행 하는 컴퓨터의 순서</span><span class="sxs-lookup"><span data-stu-id="4b5b6-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="4b5b6-135">Sequencer를 설치 하기 전에 터미널 서비스를 실행 하는 컴퓨터에서 설치 모드를 구성 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="4b5b6-136">시퀀싱 모범 사례</span><span class="sxs-lookup"><span data-stu-id="4b5b6-136">Sequencing Best Practices</span></span>


<span data-ttu-id="4b5b6-137">새 응용 프로그램을 시퀀싱 하는 경우 다음과 같은 모범 사례를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="4b5b6-138">**참고**  App-v 4.6 SP1을 실행 중인 경우에는 8.3 명명 규칙을 따르는 디렉터리로 순서를 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="4b5b6-139">8.3 명명 규칙을 따르는 고유 디렉터리에 대 한 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="4b5b6-140">모든 응용 프로그램을 8.3 명명 규칙을 따르는 디렉터리로 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="4b5b6-141">지정 된 디렉터리 이름에는 8 자 보다 많은 문자를 포함할 수 없으며, 그 뒤에 3 자의 파일 이름 확장명 (예: Q:\\MYAPP.)이 있습니다. \*\* ABC\*\*.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="4b5b6-142">하위 디렉터리가 아닌 드라이브의 루트에 있는 대상 폴더에 대 한 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="4b5b6-143">응용 프로그램 제품군에 여러 부분이 있는 경우 각 응용 프로그램을 주 디렉터리의 하위 디렉터리에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="4b5b6-144">예를 들어 패키지에 클라이언트와 함께 응용 프로그램이 포함 된 경우 **Q:\\AppSuite** 를 주 디렉터리로 사용 하 고 기본 응용 프로그램을 **Q:\\AppSuite\\Main**로 시퀀스 하 고 클라이언트를 **Q:\\AppSuite\\Client**로 시퀀싱 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="4b5b6-145">설치 단계 중에 응용 프로그램을 구성 하 고 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="4b5b6-146">응용 프로그램 설치를 완료 하는 경우 응용 프로그램 설치 프로세스에 포함 되지 않는 몇 가지 수동 단계를 수행 해야 하는 경우가 자주 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="4b5b6-147">이러한 단계에는 데이터베이스에 대 한 연결을 구성 하거나 업데이트 된 파일을 복사할 수 있는 단계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="4b5b6-148">설치 단계 중에 이러한 구성을 수행한 다음 응용 프로그램을 실행 하 여 작동 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="4b5b6-149">필요한 경우 프로그램이 안정적이 될 때까지 응용 프로그램을 여러 번 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="4b5b6-150">설치 중에는 응용 프로그램을 여러 번 실행 하 여 연결 된 모든 등록 및 대화 상자 구성이 완료 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="4b5b6-151">설치 중에 응용 프로그램을 여러 번 열면 관련 응용 프로그램 기능만 **기본 기능 블록**에 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="4b5b6-152">응용 프로그램과 연결 된 모든 자동 업데이트 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="4b5b6-153">일부 응용 프로그램에서는 설치 하는 동안 최신 업데이트를 자동으로 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="4b5b6-154">가상 응용 프로그램 패키지의 버전 관리를 지원 하려면 시퀀싱 하는 동안이 기능을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="4b5b6-155">필수 업데이트가 있는 경우 관련 업데이트가 설치 된 새 가상 응용 프로그램 패키지를 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="4b5b6-156">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4b5b6-156">Related topics</span></span>


[<span data-ttu-id="4b5b6-157">Application Virtualization 시스템 배포 계획</span><span class="sxs-lookup"><span data-stu-id="4b5b6-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





