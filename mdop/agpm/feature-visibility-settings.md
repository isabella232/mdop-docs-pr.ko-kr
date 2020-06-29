---
title: 기능 가시성 설정
description: 기능 가시성 설정
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820808"
---
# <span data-ttu-id="b7f53-103">기능 가시성 설정</span><span class="sxs-lookup"><span data-stu-id="b7f53-103">Feature Visibility Settings</span></span>


<span data-ttu-id="b7f53-104">AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하면 이러한 설정의 GPO (그룹 정책 개체)가 적용 되는 그룹 정책 관리자에 대 한 **변경 컨트롤** 노드 및 **기록** 탭의 표시 유형을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="b7f53-105">GPMC (그룹 정책 관리 콘솔)에서 GPO를 편집할 때 **그룹 정책 개체 편집기** 의 사용자 Configuration\\administrative Templates\\Windows Components\\Microsoft 관리 콘솔 \ \ 제한 된/허용 되는 Snap-ins\\Extension 스냅인에서 다음 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="b7f53-106">이 경로가 표시 되지 않으면 **관리 서식 파일**을 마우스 오른쪽 단추로 클릭 하 고 agpm 또는 agpm 템플릿을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b7f53-107">설정</span><span class="sxs-lookup"><span data-stu-id="b7f53-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="b7f53-108">효과</span><span class="sxs-lookup"><span data-stu-id="b7f53-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b7f53-109">AGPM 변경 제어</span><span class="sxs-lookup"><span data-stu-id="b7f53-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b7f53-110">이 기능을 사용 하도록 설정 하거나 구성 하지 않으면 <strong> GPMC에서 변경 내용 제어 </strong> 노드가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="b7f53-111">이 기능을 사용 하지 않도록 설정 하면 <strong> 변경 내용 제어 </strong> 노드가 GPMC에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b7f53-112">AGPM 링크 확장</span><span class="sxs-lookup"><span data-stu-id="b7f53-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b7f53-113">이 기능을 사용 하도록 설정 하거나 구성 하지 않으면 <strong> </strong> 연결 된 각 GPO에 대 한 GPMC에 기록 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="b7f53-114">이 기능을 사용 하지 않도록 설정 하면 <strong> </strong> 연결 된 gpo에 대 한 기록 탭이 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b7f53-115">AGPM GPO 확장</span><span class="sxs-lookup"><span data-stu-id="b7f53-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b7f53-116">사용 하도록 설정 하거나 구성 하지 않으면 <strong> </strong> 각 GPO에 대 한 GPMC에 기록 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="b7f53-117">사용할 수 없는 경우 <strong> , </strong> gpo에 대 한 기록 탭이 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f53-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b7f53-118">추가 참조</span><span class="sxs-lookup"><span data-stu-id="b7f53-118">Additional references</span></span>

-   [<span data-ttu-id="b7f53-119">관리 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="b7f53-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





