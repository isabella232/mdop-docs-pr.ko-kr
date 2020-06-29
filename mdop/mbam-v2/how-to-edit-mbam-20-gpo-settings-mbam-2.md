---
title: MBAM 2.0 GPO 설정을 편집하는 방법
description: MBAM 2.0 GPO 설정을 편집하는 방법
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824088"
---
# <span data-ttu-id="088be-103">MBAM 2.0 GPO 설정을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="088be-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="088be-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 먼저 Microsoft BitLocker 관리 및 모니터링 구현에서 사용할 그룹 정책을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="088be-105">사용할 수 있는 다양 한 정책에 대 한 자세한 내용은 [MBAM 2.0 그룹 정책 요구 사항 계획](planning-for-mbam-20-group-policy-requirements-mbam-2.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="088be-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="088be-106">사용할 정책을 결정 한 후에는 MBAM에 대 한 정책 설정을 포함 하는 하나 이상의 GPO (그룹 정책 개체)를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="088be-107">다음 단계를 사용 하 여 사용자 조직의 클라이언트 컴퓨터에 대 한 BitLocker 암호화를 관리 하기 위해 MBAM을 사용 하도록 기본 권장 GPO 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="088be-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="088be-108">MBAM 클라이언트 GPO 설정을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="088be-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="088be-109">MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="088be-110">MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 제품을 사용 하 고, **컴퓨터 구성을**선택 하 고, **정책을**선택 하 고, **관리 템플릿을**클릭 하 고, **Windows 구성 요소**를 선택한 다음 **MDOP mbam (BitLocker Management)** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="088be-111">클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 개체 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="088be-112">다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 **정책을**클릭 한 다음 **설정을**구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="088be-113">정책 그룹</span><span class="sxs-lookup"><span data-stu-id="088be-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="088be-114">정책</span><span class="sxs-lookup"><span data-stu-id="088be-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="088be-115">설정</span><span class="sxs-lookup"><span data-stu-id="088be-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="088be-116">클라이언트 관리</span><span class="sxs-lookup"><span data-stu-id="088be-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-117">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="088be-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-118">활성화.</span><span class="sxs-lookup"><span data-stu-id="088be-118">Enabled.</span></span> <span data-ttu-id="088be-119"><strong>Mbam 복구 및 하드웨어 서비스 끝점 </strong> 을 설정 하 고 <strong> 저장할 BitLocker 복구 정보를 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="088be-120"><strong>Mbam 준수 서비스 끝점 </strong> 을 설정 하 고 상태 보고서 빈도를 (분)에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="088be-121">운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="088be-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-122">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="088be-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-123">활성화.</span><span class="sxs-lookup"><span data-stu-id="088be-123">Enabled.</span></span> <span data-ttu-id="088be-124"><strong>운영 체제 드라이브에 대 한 선택 보호 기능을 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="088be-125">운영 체제 드라이브 데이터를 MBAMKey 복구 서버에 저장 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="088be-126">이동식 드라이브</span><span class="sxs-lookup"><span data-stu-id="088be-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-127">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="088be-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-128">활성화.</span><span class="sxs-lookup"><span data-stu-id="088be-128">Enabled.</span></span> <span data-ttu-id="088be-129">MBAM이 MBAM 키 복구 서버에 이동식 드라이브 데이터를 저장 하는 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="088be-130">고정식 드라이브</span><span class="sxs-lookup"><span data-stu-id="088be-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-131">고정 드라이브의 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="088be-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="088be-132">활성화.</span><span class="sxs-lookup"><span data-stu-id="088be-132">Enabled.</span></span> <span data-ttu-id="088be-133">MBAM은 고정 드라이브 데이터를 MBAM 키 복구 서버에 저장 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="088be-134">설정 <strong> BitLocker로 보호 되는 드라이브를 복구 하 </strong> 고 <strong> 데이터 복구 에이전트를 허용 하는 방법을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="088be-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="088be-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="088be-135">Related topics</span></span>


[<span data-ttu-id="088be-136">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="088be-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









