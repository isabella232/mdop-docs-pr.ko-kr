---
title: MBAM 2.5 그룹 정책 설정 편집
description: MBAM 2.5 그룹 정책 설정 편집
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812596"
---
# <span data-ttu-id="2b665-103">MBAM 2.5 그룹 정책 설정 편집</span><span class="sxs-lookup"><span data-stu-id="2b665-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="2b665-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2b665-105">작업</span><span class="sxs-lookup"><span data-stu-id="2b665-105">Task</span></span></th>
<th align="left"><span data-ttu-id="2b665-106">추가 정보</span><span class="sxs-lookup"><span data-stu-id="2b665-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2b665-107">MBAM 2.5 그룹 정책 템플릿을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="2b665-108">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="2b665-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2b665-109">MBAM 구현에 사용 하려는 Gpo (그룹 정책 개체)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="2b665-110">조직의 요구 사항에 따라 추가 그룹 정책 설정을 구성 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="2b665-111">MBAM 2.5 그룹 정책 요구 사항 계획 </a> – gpo에 대 한 설명이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2b665-112">조직의 그룹 정책 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2b665-113">**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="2b665-114">**MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="2b665-115">MBAM 클라이언트 그룹 정책 설정을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="2b665-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="2b665-116">MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="2b665-117">Mbam 그룹 정책 템플릿이 설치 된 컴퓨터에서 GPMC (그룹 정책 관리 콘솔) 또는 Microsoft 고급 그룹 정책 관리 MDOP 제품을 사용 하 여 **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** , &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker 관리)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="2b665-118">클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="2b665-119">다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 원하는 **정책을** 클릭 한 다음 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2b665-120">정책 그룹</span><span class="sxs-lookup"><span data-stu-id="2b665-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="2b665-121">정책</span><span class="sxs-lookup"><span data-stu-id="2b665-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2b665-122">클라이언트 관리</span><span class="sxs-lookup"><span data-stu-id="2b665-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b665-123">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="2b665-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2b665-124">운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="2b665-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b665-125">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="2b665-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2b665-126">이동식 드라이브</span><span class="sxs-lookup"><span data-stu-id="2b665-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b665-127">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="2b665-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2b665-128">고정식 드라이브</span><span class="sxs-lookup"><span data-stu-id="2b665-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b665-129">고정 드라이브의 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="2b665-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="2b665-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2b665-130">Related topics</span></span>


[<span data-ttu-id="2b665-131">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="2b665-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="2b665-132">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="2b665-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="2b665-133">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="2b665-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2b665-134">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2b665-135">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b665-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





