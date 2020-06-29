---
title: Sequencer 설치 방법
description: Sequencer 설치 방법
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817268"
---
# <span data-ttu-id="bb353-103">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="bb353-103">How to Install the Sequencer</span></span>


<span data-ttu-id="bb353-104">Microsoft App-v (Application Virtualization) Sequencer는 응용 프로그램을 가상 응용 프로그램으로 실행할 수 있도록 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="bb353-105">운영 체제만 설치 되어 있는 컴퓨터에 시퀀서를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="bb353-106">또는 가상 환경을 실행 하는 컴퓨터 (예: Microsoft 가상 PC)에 시퀀서를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="bb353-107">이 메서드는 최소한의 추가 구성으로 재사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="bb353-108">응용 프로그램을 시퀀싱 하는 데 사용 하는 컴퓨터에 대 한 관리자 권한이 있어야 하 고 컴퓨터가 네트워크에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="bb353-109">컴퓨터는 Application Virtualization (App-v) 클라이언트 버전을 실행 하 고 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="bb353-110">시퀀서를 사용 하 여 가상 응용 프로그램을 만드는 것은 매우 많은 리소스를 필요로 하므로 권장 요구 사항을 충족 하거나 초과 하는 컴퓨터에 시퀀서를 설치 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="bb353-111">시스템 요구 사항에 대 한 자세한 내용은 [Sequencer 하드웨어 및 소프트웨어 요구 사항을](sequencer-hardware-and-software-requirements.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb353-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="bb353-112">Microsoft Application Virtualization Sequencer를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="bb353-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="bb353-113">설치 하려는 컴퓨터에 Microsoft Application Virtualization Sequencer 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="bb353-114">Microsoft Application Virtualization Sequencer 설치 마법사를 시작 하려면 **setup.exe**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="bb353-115">설치 전에 **Microsoft Visual c + + SP1 재배포 가능 패키지 (x86)** 가 검색 되지 않으면 **setup.exe** 에서 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="bb353-116">**시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="bb353-117">**사용권 계약 페이지에서** 사용권 계약 조건에 동의 **하려면 동의 함을 선택 합니다**.</span><span class="sxs-lookup"><span data-stu-id="bb353-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="bb353-118">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-118">Click **Next**.</span></span>

5.  <span data-ttu-id="bb353-119">**대상 폴더** 페이지에서 기본 설치 폴더를 그대로 사용 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="bb353-120">다른 대상 폴더를 지정 하려면 **변경을** 클릭 하 고 설치에 사용 될 설치 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="bb353-121">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-121">Click **Next**.</span></span>

6.  <span data-ttu-id="bb353-122">**프로그램 설치 준비** 페이지에서 설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="bb353-123">**InstallShield 마법사 완료** 페이지에서 설치 마법사를 닫고 시퀀서를 열려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="bb353-124">Sequencer를 열지 않고 설치 마법사를 닫으려면 **프로그램 실행** 을 선택 취소 하 고 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb353-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="bb353-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bb353-125">Related topics</span></span>


[<span data-ttu-id="bb353-126">Application Virtualization Sequencer 구성</span><span class="sxs-lookup"><span data-stu-id="bb353-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





