---
title: Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소
description: Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812564"
---
# <span data-ttu-id="b4583-103">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="b4583-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="b4583-104">System Center Configuration Manager 통합 기능을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하는 경우 [독립 실행형 및 구성 관리자 통합 토폴로지에 대해 mbam 2.5 Server 필수 구성 요소와](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)함께이 항목에서 설명 하는 필수 구성 요소를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="b4583-105">또한 Configuration Manager 통합 토폴로지에 필요한 .mof 파일을 만들거나 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="b4583-106">Configuration Manager 통합 기능의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="b4583-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="b4583-107">System Center Configuration Manager 통합 토폴로지로 MBAM을 구성 하는 경우에는 구성 관리자에 필요한 추가 필수 구성 요소를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="b4583-108">Configuration Manager 통합 기능의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="b4583-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="b4583-109">구성 .mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="b4583-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="b4583-110">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면 SystemCenter2012 ConfigurationManager 및 Microsoft System Center Configuration Manager 2007에 대 한 구성. mof 파일을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="b4583-111">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="b4583-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="b4583-112">Sms \ _def .mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="b4583-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="b4583-113">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서에서 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면, Sms \ _def .mof 파일을 만들거나 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="b4583-114">SystemCenter2012 ConfigurationManager를 사용 하는 경우에는 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="b4583-115">Configuration Manager 2007에서 파일이 이미 있으므로 기존 파일을 편집 하 고 덮어쓰지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="b4583-116">Sms \ _def .mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="b4583-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="b4583-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b4583-117">Related topics</span></span>


[<span data-ttu-id="b4583-118">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="b4583-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="b4583-119">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="b4583-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="b4583-120">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="b4583-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="b4583-121">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="b4583-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b4583-122">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b4583-123">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4583-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




