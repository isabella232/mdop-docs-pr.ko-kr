---
title: 관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법
description: 관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법
author: dansimp
ms.assetid: 42ca3157-5d85-467b-a148-09404f8f737a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 083d6386f02996d35255f90958705798f2cd5fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814452"
---
# <span data-ttu-id="5fc6e-103">관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법</span><span class="sxs-lookup"><span data-stu-id="5fc6e-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="5fc6e-104">관리자 (최종 사용자가 아님)만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있도록 App-v 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="5fc6e-105">이전 버전의 App-v에서는 최종 사용자가 이러한 작업을 수행 하는 것을 방지할 수 없었습니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="5fc6e-106">**참고** 
 **이 기능은 app-v 5.0 SP3에서 시작 하는 것으로 지원 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="5fc6e-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="5fc6e-107">다음 방법 중 하나를 사용 하 여 관리자만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5fc6e-108">메서드</span><span class="sxs-lookup"><span data-stu-id="5fc6e-108">Method</span></span></th>
<th align="left"><span data-ttu-id="5fc6e-109">단계</span><span class="sxs-lookup"><span data-stu-id="5fc6e-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5fc6e-110">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5fc6e-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fc6e-111">다음 그룹 정책 개체 노드에 있는 "관리자로 게시 필요" 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="5fc6e-112">컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시</span><span class="sxs-lookup"><span data-stu-id="5fc6e-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5fc6e-113">PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5fc6e-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="5fc6e-114"><strong> </strong> <strong> – RequireAppvClientConfiguration cmdlet 관리자 매개 변수를 사용 하 여 명령줄을 실행 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="5fc6e-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="5fc6e-115">매개 변수 값:</span><span class="sxs-lookup"><span data-stu-id="5fc6e-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="5fc6e-116">0-거짓</span><span class="sxs-lookup"><span data-stu-id="5fc6e-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="5fc6e-117">1-참</span><span class="sxs-lookup"><span data-stu-id="5fc6e-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5fc6e-118">예: </strong> : Set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="5fc6e-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5fc6e-119">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="5fc6e-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5fc6e-120">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5fc6e-121">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="5fc6e-121">Got an App-V issue?</span></span>** <span data-ttu-id="5fc6e-122">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc6e-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5fc6e-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5fc6e-123">Related topics</span></span>


[<span data-ttu-id="5fc6e-124">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="5fc6e-124">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





