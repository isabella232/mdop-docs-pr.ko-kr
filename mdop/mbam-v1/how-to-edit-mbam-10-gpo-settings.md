---
title: MBAM 1.0 GPO 설정을 편집하는 방법
description: MBAM 1.0 GPO 설정을 편집하는 방법
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824283"
---
# <span data-ttu-id="7331b-103">MBAM 1.0 GPO 설정을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="7331b-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="7331b-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 먼저 Microsoft BitLocker 관리 및 모니터링 구현에서 사용할 그룹 정책을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="7331b-105">사용할 수 있는 다양 한 정책에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7331b-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="7331b-106">사용할 정책을 결정 한 후에는 MBAM 정책 설정을 포함 하는 하나 이상의 GPO (그룹 정책 개체)를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="7331b-107">다음 단계에서는 MBAM이 조직의 클라이언트 컴퓨터에 대 한 BitLocker 암호화를 관리할 수 있도록 기본 GPO (권장 그룹 정책 개체) 설정을 구성 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="7331b-108">MBAM 클라이언트 GPO 설정을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="7331b-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="7331b-109">MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="7331b-110">그룹 정책 관리 콘솔 (GPMC) 또는 AGPM (고급 그룹 정책 관리) MDOP 제품을 사용 하 여 다음 작업을 수행 합니다. **컴퓨터 구성**선택, **정책**, **관리 템플릿**, **Windows 구성 요소**를 차례로 선택한 다음 **MDOP mbam (BitLocker Management)** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="7331b-111">클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 개체 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="7331b-112">다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 **정책을**클릭 한 다음 **설정을**구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="7331b-113">정책 그룹</span><span class="sxs-lookup"><span data-stu-id="7331b-113">Policy Group</span></span>

    <span data-ttu-id="7331b-114">정책</span><span class="sxs-lookup"><span data-stu-id="7331b-114">Policy</span></span>

    <span data-ttu-id="7331b-115">설정</span><span class="sxs-lookup"><span data-stu-id="7331b-115">Setting</span></span>

    <span data-ttu-id="7331b-116">클라이언트 관리</span><span class="sxs-lookup"><span data-stu-id="7331b-116">Client Management</span></span>

    <span data-ttu-id="7331b-117">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="7331b-117">Configure MBAM Services</span></span>

    <span data-ttu-id="7331b-118">활성화.</span><span class="sxs-lookup"><span data-stu-id="7331b-118">Enabled.</span></span> <span data-ttu-id="7331b-119">**Mbam 복구 및 하드웨어 서비스 끝점** 을 설정 하 고 **저장할 BitLocker 복구 정보를 선택**합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="7331b-120">**Mbam 준수 서비스 끝점** 을 설정 하 고 **상태 보고서 빈도를 (분)에 입력**합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="7331b-121">하드웨어 호환성 검사 허용</span><span class="sxs-lookup"><span data-stu-id="7331b-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="7331b-122">사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-122">Disabled.</span></span> <span data-ttu-id="7331b-123">이 정책은 기본적으로 사용 하도록 설정 되어 있지만 기본 MBAM 구현에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="7331b-124">운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="7331b-124">Operating System Drive</span></span>

    <span data-ttu-id="7331b-125">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="7331b-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="7331b-126">활성화.</span><span class="sxs-lookup"><span data-stu-id="7331b-126">Enabled.</span></span> <span data-ttu-id="7331b-127">**운영 체제 드라이브에 대 한 선택 보호 기능을**설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="7331b-128">이는 운영 체제 드라이브 데이터를 MBAM 키 복구 서버에 저장 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="7331b-129">이동식 드라이브</span><span class="sxs-lookup"><span data-stu-id="7331b-129">Removable Drive</span></span>

    <span data-ttu-id="7331b-130">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="7331b-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="7331b-131">활성화.</span><span class="sxs-lookup"><span data-stu-id="7331b-131">Enabled.</span></span> <span data-ttu-id="7331b-132">이는 MBAM이 이동식 드라이브 데이터를 Mbam 복구 서버에 저장 하는 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="7331b-133">고정식 드라이브</span><span class="sxs-lookup"><span data-stu-id="7331b-133">Fixed Drive</span></span>

    <span data-ttu-id="7331b-134">고정 드라이브의 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="7331b-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="7331b-135">활성화.</span><span class="sxs-lookup"><span data-stu-id="7331b-135">Enabled.</span></span> <span data-ttu-id="7331b-136">이는 MBAM이 고정 드라이브 데이터를 Mbam 복구 서버에 저장 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="7331b-137">설정 **BitLocker로 보호 되는 드라이브를 복구 하** 고 **데이터 복구 에이전트를 허용**하는 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7331b-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="7331b-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7331b-138">Related topics</span></span>


[<span data-ttu-id="7331b-139">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="7331b-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









