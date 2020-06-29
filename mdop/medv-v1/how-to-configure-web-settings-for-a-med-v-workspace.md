---
title: MED-V 작업 영역에 대한 웹 설정을 구성하는 방법
description: MED-V 작업 영역에 대한 웹 설정을 구성하는 방법
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827068"
---
# <span data-ttu-id="461cd-103">MED-V 작업 영역에 대한 웹 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="461cd-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="461cd-104">이전 버전의 Internet Explorer 에서만 표시할 수 있고 호스트 운영 체제에는 없는 웹 사이트는 MED-V 작업 영역 내에 있는 이전 버전의 Internet Explorer에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="461cd-105">사용자가 MED-V 작업 영역에서 브라우저를 열지 않아도 지정 된 웹 사이트를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="461cd-106">사용자는 호스트에서 브라우저를 열고 MED-V 작업 영역으로 자동으로 리디렉션되고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="461cd-107">다음 절차에서는 MED-V 작업 영역의 웹 검색 규칙 목록을 설정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="461cd-108">규칙에 포함 된 모든 사이트는 MED-V 작업 영역이 나 관리자가 정의한 호스트에서 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="461cd-109">규칙 내에 정의 되지 않은 모든 사이트는 해당 사이트가 요청 된 환경에서 탐색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="461cd-110">그러나이를 그룹으로 구성 하 여 MED-V 작업 영역이 나 호스트에서 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="461cd-111">참고</span><span class="sxs-lookup"><span data-stu-id="461cd-111">Note</span></span>**  
<span data-ttu-id="461cd-112">웹 설정은 Internet Explorer 및 다른 브라우저에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="461cd-113">모든 웹 설정은 **정책** 모듈의 **웹** 탭에 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="461cd-114">MED-V 작업 영역에 대 한 웹 설정을 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="461cd-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="461cd-115">MED-V 작업 영역에 대 한 웹 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="461cd-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="461cd-116">구성할 MED-V 작업 영역을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="461cd-117">사용자가 지정 된 웹 규칙을 준수 하는 URL을 탐색할 때 사용자를 MED-V 작업 영역 또는 호스트 내의 브라우저로 리디렉션하려면 **다음 표에 정의 된 url 목록 검색** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="461cd-118">다음 중 하나를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-118">Click one of the following:</span></span>

    -   <span data-ttu-id="461cd-119">**작업 영역에서**-med-v 작업 영역의 브라우저로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="461cd-120">**호스트에서**-호스트의 브라우저로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="461cd-121">**다른 모든 Url 찾아보기** 확인란을 선택 하 여 웹 규칙에서 제외한 모든 url을 호스트 또는 med-v 작업 영역으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="461cd-122">다음 중 하나를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-122">Click one of the following:</span></span>

    -   <span data-ttu-id="461cd-123">**작업 영역에서**-다른 모든 URL을 med-v 작업 영역의 브라우저로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="461cd-124">**호스트에서**— 다른 모든 url을 호스트의 브라우저로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="461cd-125">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="461cd-126">웹 규칙을 추가 하는 방법</span><span class="sxs-lookup"><span data-stu-id="461cd-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="461cd-127">웹 규칙을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="461cd-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="461cd-128">**다음 표에 정의 된 url 목록 찾아보기** 확인란을 선택 하 여 웹 검색 규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="461cd-129">**추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-129">Click **Add**.</span></span>

    <span data-ttu-id="461cd-130">새 웹 규칙이 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="461cd-131">다음 표의 설명 대로 웹 규칙 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="461cd-132">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="461cd-133">MED-V 작업 영역 웹 속성</span><span class="sxs-lookup"><span data-stu-id="461cd-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="461cd-134">속성</span><span class="sxs-lookup"><span data-stu-id="461cd-134">Property</span></span></th>
<th align="left"><span data-ttu-id="461cd-135">설명</span><span class="sxs-lookup"><span data-stu-id="461cd-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="461cd-136">유형</span><span class="sxs-lookup"><span data-stu-id="461cd-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="461cd-137">도메인 접미사 </strong> -Value 속성에 지정 된 접미사로 끝나는 모든 호스트 주소에 대 <strong> </strong> 한 액세스 이며 웹 검색의 옵션 집합에 따라 설정 됩니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="461cd-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="461cd-138">IP 접두사 </strong> -Value 속성에 지정 된 접두사 범위에서 전체 또는 부분 IP 주소에 액세스 하 <strong> </strong> 고 웹 검색에 설정 된 옵션에 따라 설정 됩니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="461cd-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="461cd-139">모든 로컬 주소 </strong> -&#39; 없이 모든 주소에 액세스 하며, 웹 검색의 옵션 집합에 따라 설정 됩니다 &#39;. <strong> </strong></span><span class="sxs-lookup"><span data-stu-id="461cd-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="461cd-140">값</span><span class="sxs-lookup"><span data-stu-id="461cd-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="461cd-141"><strong> </strong> Type 속성에 도메인 접미사가 선택 되어 <strong> 있으면 </strong> 도메인 접미사를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="461cd-142">참고</span><span class="sxs-lookup"><span data-stu-id="461cd-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="461cd-143">&quot; \* &quot; 접미사 앞에 입력 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="461cd-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="461cd-144">도메인 접미사는 별칭도 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="461cd-145">Type 속성에서 IP 접두사를 선택한 <strong> 경우 </strong> 전체 또는 일부 ip 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="461cd-146">웹 규칙을 삭제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="461cd-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="461cd-147">웹 규칙을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="461cd-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="461cd-148">**웹** 창에서 삭제할 웹 규칙을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="461cd-149">**제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-149">Click **Remove**.</span></span>

    <span data-ttu-id="461cd-150">웹 규칙이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="461cd-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="461cd-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="461cd-151">Related topics</span></span>


[<span data-ttu-id="461cd-152">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="461cd-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="461cd-153">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="461cd-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









