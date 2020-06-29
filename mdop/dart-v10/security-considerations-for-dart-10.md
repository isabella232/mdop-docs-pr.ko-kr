---
title: DaRT 10에 대한 보안 고려 사항
description: DaRT 10에 대한 보안 고려 사항
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823053"
---
# <span data-ttu-id="d945b-103">DaRT 10에 대한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d945b-103">Security Considerations for DaRT 10</span></span>


<span data-ttu-id="d945b-104">이 항목에서는 계정 및 그룹, 로그 파일 및 Microsoft 진단 및 복구 도구 집합 (DaRT) 10의 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span> <span data-ttu-id="d945b-105">자세한 내용은이 문서에 나와 있는 링크를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="d945b-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="d945b-106">일반 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d945b-106">General security considerations</span></span>


<span data-ttu-id="d945b-107">**보안 위험을 파악**합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-107">**Understand the security risks**.</span></span> <span data-ttu-id="d945b-108">DaRT 10에는 관리자 또는 지원 센터에서 DaRT 도구를 원격으로 실행 하 여 최종 사용자 컴퓨터의 문제를 해결할 수 있는 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-108">DaRT 10 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="d945b-109">또한 ISO (국제 표준화 기구) 이미지를 USB 플래시 드라이브에 저장 하거나 ISO 이미지를 컴퓨터의 하드 디스크에 복구 파티션으로 포함 하도록 네트워크에 넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="d945b-110">이러한 접근 권한 값은 유연성을 제공 하지만, DaRT를 구성할 때 고려해 야 하는 잠재적인 보안 위험을 생성 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="d945b-111">**컴퓨터를 물리적으로 보호**합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-111">**Physically secure your computers**.</span></span> <span data-ttu-id="d945b-112">관리자와 헬프 데스크 근로자가 물리적으로 컴퓨터에 있지 않은 경우 컴퓨터를 잠그고 안전한 화면 보호기를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="d945b-113">**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="d945b-114">보안 알림 서비스 ()에 가입 하 여 운영 체제에 대 한 새로운 업데이트에 대 한 정보를 지속적으로 유지 <https://go.microsoft.com/fwlink/?LinkId=28819> 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="d945b-115">Office 도구에 대 한 최종 사용자 액세스 제한</span><span class="sxs-lookup"><span data-stu-id="d945b-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="d945b-116">DaRT 복구 이미지를 만들 때 포함 하려는 도구를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="d945b-117">보안상의 이유로, 최종 사용자 액세스를 디스크 지우기 및 Locksmith와 같은 강력한 DaRT 도구에 대해 제한 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="d945b-118">DaRT 10에서는 구성 중 특정 도구를 사용 하지 않도록 설정할 수 있으며, 최종 사용자가 원격 연결 기능을 시작할 때 지원 센터에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-118">In DaRT 10, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="d945b-119">원격 연결 세션을 시작 하는 옵션이 최종 사용자에 게 제공 되는 유일한 도구인 DaRT 이미지를 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="d945b-120">**중요**  원격 연결이 설정 되 면 최종 사용자에 게 사용할 수 없는 작업을 포함 하 여 복구 이미지에 포함 된 모든 도구가 최종 사용자 컴퓨터에서 작동 하는 모든 지원 센터 작업자에 게 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="d945b-121">DaRT 복구 이미지의 도구를 포함 하는 방법에 대 한 자세한 내용은 [dart 10의 도구 개요](overview-of-the-tools-in-dart-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d945b-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

## <span data-ttu-id="d945b-122">DaRT 복구 이미지 보안</span><span class="sxs-lookup"><span data-stu-id="d945b-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="d945b-123">USB 플래시 드라이브에 DaRT 복구 이미지를 저장 하거나 원격 파티션이나 복구 파티션을 만들어 배포 하는 경우 회사의 선호 하는 드라이브 암호화 방법을 ISO에 포함 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="d945b-124">ISO를 암호화 하면 최종 사용자가 복구 이미지에 대 한 액세스 권한을 얻은 경우 DaRT 기능을 사용할 수 없으며, 다른 사람에 속한 컴퓨터에서 권한이 없는 사용자가 DaRT로 부팅 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="d945b-125">암호화 방법을 사용 하는 경우 모든 컴퓨터에서이를 배포 하 고 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="d945b-126">**참고**  DaRT 10은 BitLocker를 기본적으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-126">**Note** DaRT 10 supports BitLocker natively.</span></span>

 

<span data-ttu-id="d945b-127">드라이브 암호화를 포함 하려면 복구 이미지를 만들 때 암호화 솔루션 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="d945b-128">암호화 솔루션은 WinPE에서 실행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="d945b-129">ISO에서 부팅 하는 최종 사용자는 해당 암호화 솔루션에 액세스 하 고 드라이브 차단을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="d945b-130">원격 연결을 사용할 때 두 컴퓨터 간의 보안 유지</span><span class="sxs-lookup"><span data-stu-id="d945b-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="d945b-131">기본적으로 **원격 연결** 세션을 설정한 두 컴퓨터 간의 통신은 암호화 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="d945b-132">따라서 두 컴퓨터 간의 보안을 유지 하기 위해 두 컴퓨터를 같은 네트워크에 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d945b-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="d945b-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d945b-133">Related topics</span></span>


[<span data-ttu-id="d945b-134">DaRT 10에 대한 보안 및 개인 정보</span><span class="sxs-lookup"><span data-stu-id="d945b-134">Security and Privacy for DaRT 10</span></span>](security-and-privacy-for-dart-10.md)

 

 





