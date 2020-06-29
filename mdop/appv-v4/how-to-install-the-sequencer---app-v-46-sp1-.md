---
title: Sequencer를 설치 하는 방법 (App-v 4.6 SP1)
description: Sequencer를 설치 하는 방법 (App-v 4.6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817273"
---
# <span data-ttu-id="0c790-103">Sequencer를 설치 하는 방법 (App-v 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="0c790-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="0c790-104">Microsoft App-v (Application Virtualization) Sequencer는 응용 프로그램을 가상 응용 프로그램으로 실행할 수 있도록 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="0c790-105">운영 체제만 설치 되어 있는 컴퓨터에는 App-v Sequencer를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="0c790-106">또는 가상 환경 (예: 가상 컴퓨터)에서 실행 되는 컴퓨터에 시퀀서를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="0c790-107">이 방법은 최소한의 추가 구성으로 다시 사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="0c790-108">응용 프로그램을 시퀀싱 하는 데 사용 하는 컴퓨터에 대 한 관리자 자격 증명이 있어야 하 고, 컴퓨터는 모든 버전의 App-v 클라이언트를 실행 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="0c790-109">App-v 시퀀서를 사용 하 여 가상 응용 프로그램을 만들려면 여러 작업을 수행 해야 하므로 [Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항을](application-virtualization-sequencer-hardware-and-software-requirements.md)충족 하거나 초과 하는 컴퓨터에 시퀀서를 설치 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="0c790-110">참고</span><span class="sxs-lookup"><span data-stu-id="0c790-110">Note</span></span>**  
<span data-ttu-id="0c790-111">안전 모드에서 App-v 시퀀서를 실행 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="0c790-112">Microsoft Application Virtualization Sequencer를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="0c790-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="0c790-113">설치 하려는 컴퓨터에 Microsoft Application Virtualization Sequencer 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="0c790-114">Microsoft Application Virtualization Sequencer 설치 마법사를 시작 하려면 **Setup.exe**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="0c790-115">설치 전에 **Microsoft Visual c + + SP1 재배포 가능 패키지 (x86)** 가 검색 되지 않는 경우 **설치** 를 클릭 하 여 필수 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="0c790-116">설치를 계속 하려면 **시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="0c790-117">**사용권 계약 페이지에서** 사용권 계약 약관에 동의 하는 경우 **동의**함을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="0c790-118">**대상 폴더** 페이지에서 기본 설치 폴더를 그대로 사용 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="0c790-119">다른 대상 폴더를 지정 하려면 **변경을** 클릭 하 고 설치에 사용 될 설치 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="0c790-120">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-120">Click **Next**.</span></span>

6.  <span data-ttu-id="0c790-121">**가상 드라이브** 페이지에서 응용 프로그램 가상화 기본 드라이브 **Q:\\** (기본값)를 모든 시퀀싱 된 응용 프로그램이 실행 되는 드라이브로 구성 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="0c790-122">다른 드라이브 문자를 지정 하려면 목록을 사용 하 고 적절 한 드라이브 문자를 선택 하 여 사용할 드라이브 문자를 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="0c790-123">중요</span><span class="sxs-lookup"><span data-stu-id="0c790-123">Important</span></span>**  
    <span data-ttu-id="0c790-124">이 단계에서 지정 하는 Application Virtualization 드라이브 문자는 가상 응용 프로그램이 대상 컴퓨터에서 실행 되는 드라이브 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="0c790-125">지정 된 드라이브 문자를 사용할 수 있어야 하며, 현재 App-v 클라이언트를 실행 하는 컴퓨터에서 사용 중이 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="0c790-126">지정 된 드라이브가 이미 사용 중인 경우 가상 응용 프로그램은 대상 컴퓨터에서 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="0c790-127">**프로그램 설치 준비** 페이지에서 설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="0c790-128">**InstallShield 마법사 완료** 페이지에서 설치 마법사를 닫고 app-v Sequencer를 열려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="0c790-129">Sequencer를 열지 않고 설치 마법사를 닫으려면 **프로그램 실행**을 선택 취소 하 고 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="0c790-130">참고</span><span class="sxs-lookup"><span data-stu-id="0c790-130">Note</span></span>**  
    <span data-ttu-id="0c790-131">가상 환경을 실행 하는 컴퓨터 (예: 가상 컴퓨터)에 App-v 시퀀서를 설치한 경우 이제 스냅숏을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="0c790-132">응용 프로그램을 순서 대로 만들면 다음 응용 프로그램의 순서를 지정할 수 있도록이 이미지로 되돌릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c790-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="0c790-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0c790-133">Related topics</span></span>


[<span data-ttu-id="0c790-134">Application Virtualization Sequencer(App-V 4.6 SP1) 구성</span><span class="sxs-lookup"><span data-stu-id="0c790-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









