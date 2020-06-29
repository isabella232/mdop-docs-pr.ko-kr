---
title: DaRT 7.0에 대한 보안 고려 사항
description: DaRT 7.0에 대한 보안 고려 사항
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822733"
---
# <span data-ttu-id="f3ecb-103">DaRT 7.0에 대한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="f3ecb-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="f3ecb-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7에는 관리자가 DaRT 도구를 원격으로 실행 하 여 최종 사용자 컴퓨터의 문제를 해결할 수 있는 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="f3ecb-105">이전 버전의 DaRT에서는 헬프 데스크 기술자 또는 관리자가 물리적으로 최종 사용자 컴퓨터에 있어야 하 고 DaRT 복구 이미지를 포함 하는 CD 또는 DVD를 사용 하 여 DaRT로 부팅 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="f3ecb-106">이제 헬프 데스크 기술자 또는 관리자가 동일한 절차를 원격으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="f3ecb-107">또한 DaRT7에서 CD 또는 DVD를 굽는 것 외에, 이제 ISO (국제 표준화 기구) 이미지를 USB 플래시 드라이브에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="f3ecb-108">또한 ISO 이미지를 네트워크에 추가 하거나 컴퓨터 하드 디스크의 복구 파티션으로 해당 콘텐츠를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="f3ecb-109">DaRT7의 **원격 연결** 기능을 통해 최종 사용자는 이러한 새로운 배포 방법 중 하나를 사용 하 여 DaRT에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="f3ecb-110">따라서 DaRT를 더 쉽게 시작 하 고 DaRT 도구에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="f3ecb-111">DaRT7의 새로운 기능은 기업에서 DaRT를 사용 하는 방법에 훨씬 더 많은 유연성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="f3ecb-112">그러나, 처리 해야 하는 고유한 보안 문제 집합을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="f3ecb-113">DaRT를 구성할 때 다음 보안 팁을 고려 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="f3ecb-114">DaRT 복구 이미지를 만들 때 보안을 유지 하는 데 도움이 되는 방법</span><span class="sxs-lookup"><span data-stu-id="f3ecb-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="f3ecb-115">DaRT 복구 이미지를 만들 때 포함 하려는 도구를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="f3ecb-116">보안상의 이유로, 최종 사용자 액세스를 디스크 지우기 및 Locksmith와 같은 강력한 DaRT 도구에 대해 제한 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="f3ecb-117">DaRT7에서 구성 중 특정 도구를 사용 하지 않도록 설정 하 고, 최종 사용자가 원격 연결 기능을 시작할 때 헬프 데스크 상담원에 게 제공 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="f3ecb-118">원격 연결 세션을 시작 하는 옵션이 최종 사용자에 게 제공 되는 유일한 도구인 DaRT 이미지를 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="f3ecb-119">**중요**  원격 연결이 설정 되 면 최종 사용자가 사용할 수 없는 작업을 포함 하 여 복구 이미지에 포함 된 모든 도구가 최종 사용자 컴퓨터에서 작동 하는 헬프데스크 에이전트에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="f3ecb-120">DaRT 복구 이미지의 도구를 포함 하는 방법에 대 한 자세한 내용은 [Dart 복구 이미지 마법사를 사용 하 여 복구 이미지를 만드는 방법을](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="f3ecb-121">DaRT 복구 이미지를 암호화 하 여 보안을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="f3ecb-122">USB 플래시 드라이브에 저장 하거나 원격 파티션이나 복구 파티션을 만드는 등 DaRT7에서 새로 추가 된 배포 옵션 중 하나를 사용 하는 경우에는 회사의 선호 하는 드라이브 암호화 방법을 ISO에 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="f3ecb-123">이렇게 하면 최종 사용자가 복구 이미지에 대 한 액세스 권한을 획득 해야 하는 DaRT의 기능을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="f3ecb-124">또한 승인 되지 않은 사용자가 다른 사람에 속한 컴퓨터에서 DaRT로 부팅 될 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="f3ecb-125">모든 컴퓨터에서 암호화 방법을 배포 하 고 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="f3ecb-126">**참고**  DaRT7는 BitLocker를 기본적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="f3ecb-127">원격으로 연결 하는 동안 두 컴퓨터 간의 보안을 유지 하기 위해</span><span class="sxs-lookup"><span data-stu-id="f3ecb-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="f3ecb-128">기본적으로 **원격 연결** 세션을 설정한 두 컴퓨터 간의 통신은 암호화 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="f3ecb-129">따라서 두 컴퓨터 간의 보안을 유지 하기 위해 두 컴퓨터를 같은 네트워크에 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ecb-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="f3ecb-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f3ecb-130">Related topics</span></span>


[<span data-ttu-id="f3ecb-131">DaRT 7.0 작업</span><span class="sxs-lookup"><span data-stu-id="f3ecb-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





