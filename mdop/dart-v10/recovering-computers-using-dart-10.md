---
title: DaRT 10을 사용하여 컴퓨터 복구
description: DaRT 10을 사용하여 컴퓨터 복구
author: dansimp
ms.assetid: 2ad7fab0-c22d-4171-8b5a-b2b7d7c0ad2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2031d55427e24638e41dfc6ed7b0ef437922e9c4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822958"
---
# <span data-ttu-id="5d5b1-103">DaRT 10을 사용하여 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="5d5b1-103">Recovering Computers Using DaRT 10</span></span>


<span data-ttu-id="5d5b1-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지를 배포한 후에는 DaRT 10을 사용 하 여 컴퓨터를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can use DaRT 10 to recover computers.</span></span> <span data-ttu-id="5d5b1-105">이 섹션의 정보는 수행할 수 있는 복구 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="5d5b1-106">DaRT 복구 이미지를 배포 하는 방법에 따라 DaRT로 부팅 하는 데 선택할 수 있는 여러 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="5d5b1-107">DaRT 복구 이미지 CD, DVD 또는 USB 플래시 드라이브를 문제 컴퓨터에 삽입 하 고 컴퓨터를 부팅 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="5d5b1-108">문제가 있는 컴퓨터의 복구 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="5d5b1-109">네트워크의 원격 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="5d5b1-110">각 방법의 장점과 단점에 대 한 자세한 내용은 [DaRT 10 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="5d5b1-111">DaRT로 부팅 하는 데 사용 하는 방법에 관계 없이 부팅 옵션에 대 한 부팅 장치를 사용 하도록 설정 하 고 최종 사용자가 사용할 수 있도록 할 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="5d5b1-112">**참고**  BIOS 구성은 조직에 사용 되는 하드 디스크 드라이브, 네트워크 어댑터 및 기타 하드웨어의 종류에 따라 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="5d5b1-113">DaRT 복구 이미지를 사용 하 여 로컬 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="5d5b1-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="5d5b1-114">DaRT를 사용 하 여 로컬 컴퓨터를 복구 하려면 DaRT가 필요한 문제가 발생 하는 최종 사용자 컴퓨터에 실제로 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="5d5b1-115">DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="5d5b1-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md)

## <span data-ttu-id="5d5b1-116">DaRT 복구 이미지를 사용 하 여 원격 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="5d5b1-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="5d5b1-117">IT 관리자는 DaRT의 Remote Connection 기능을 사용 하 여 최종 사용자 컴퓨터에서 원격으로 DaRT 도구를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="5d5b1-118">최종 사용자가 특정 정보를 제공 하거나 (최종 사용자 컴퓨터에서 작업 하는 경우 지원 센터 전문가가), IT 관리자나 헬프 데스크 근로자가 최종 사용자의 컴퓨터를 제어 하 고 필요한 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="5d5b1-119">**중요**  원격 연결을 설정 하는 두 컴퓨터는 동일한 네트워크의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="5d5b1-120">**진단 및 복구 도구 집합** 창에는 관리자 컴퓨터에서 원격으로 최종 사용자 컴퓨터에 DaRT를 실행 하는 옵션이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="5d5b1-121">최종 사용자는 문제 컴퓨터에서 DaRT 도구를 열고 **원격 연결**을 클릭 하 여 원격 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="5d5b1-122">최종 사용자 컴퓨터의 원격 연결 기능은 티켓 번호, 포트, 사용 가능한 모든 IP 주소 목록 등의 연결 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="5d5b1-123">티켓 번호와 포트는 임의로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="5d5b1-124">IT 관리자 또는 헬프 데스크 근로자는이 정보를 **DaRT 원격 연결 뷰어에** 입력 하 여 최종 사용자 컴퓨터에 터미널 서비스 연결을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="5d5b1-125">설정 된 터미널 서비스 연결을 통해 IT 관리자가 최종 사용자 컴퓨터의 DaRT 도구와 원격으로 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="5d5b1-126">최종 사용자 컴퓨터는 연결 정보를 처리 하 고, 해당 화면을 공유 하 고, IT 관리자 컴퓨터의 지침에 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5b1-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="5d5b1-127">DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="5d5b1-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md)

## <span data-ttu-id="5d5b1-128">DaRT 10을 사용 하 여 컴퓨터를 복구 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="5d5b1-128">Other resources for recovering computers using DaRT 10</span></span>


[<span data-ttu-id="5d5b1-129">DaRT 10 작업</span><span class="sxs-lookup"><span data-stu-id="5d5b1-129">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





