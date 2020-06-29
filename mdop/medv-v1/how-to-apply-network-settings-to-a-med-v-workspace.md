---
title: MED-V 작업 영역에 네트워크 설정을 적용하는 방법
description: MED-V 작업 영역에 네트워크 설정을 적용하는 방법
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826518"
---
# <span data-ttu-id="1ba47-103">MED-V 작업 영역에 네트워크 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="1ba47-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="1ba47-104">관리자는 각 MED-V 작업 영역에 대 한 네트워크 설정을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="1ba47-105">**네트워크 탭의** **정책** 모듈에서 모든 네트워크 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="1ba47-106">MED-V 작업 영역에 네트워크 설정을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="1ba47-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="1ba47-107">MED-V 작업 영역을 클릭 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="1ba47-108">**네트워크** 창에서 다음 표에 설명 된 대로 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="1ba47-109">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="1ba47-110">MED-V 작업 영역 네트워크 속성</span><span class="sxs-lookup"><span data-stu-id="1ba47-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ba47-111">속성</span><span class="sxs-lookup"><span data-stu-id="1ba47-111">Property</span></span></th>
<th align="left"><span data-ttu-id="1ba47-112">설명</span><span class="sxs-lookup"><span data-stu-id="1ba47-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ba47-113">TCP/IP 속성</span><span class="sxs-lookup"><span data-stu-id="1ba47-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="1ba47-114">호스트의 IP 주소 (NAT) 사용 </strong> -작업 영역에서 nat를 사용 하 여 송신 트래픽에 대 한 호스트의 IP를 공유 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="1ba47-115">호스트와 다른 IP 주소 사용 (브리지) </strong> -med-v 작업 영역에는 일반적으로 DHCP를 통해 얻을 수 있는 고유한 네트워크 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="1ba47-116"><strong>호스트 컴퓨터에 여러 어댑터가 있으면 작업 영역에 여러 어댑터 매핑 확인란을 선택 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ba47-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="1ba47-117">호스트가 다른 어댑터를 사용 하는 다른 네트워크 간을 이동할 때이 구성을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ba47-118">DNS 서버</span><span class="sxs-lookup"><span data-stu-id="1ba47-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="1ba47-119">변경 안 함 </strong> -med-v 작업 영역에 설정 된 DNS 설정은 가상 컴퓨터에서 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="1ba47-120">호스트의 DNS 주소 사용 </strong> -med-v 작업 영역 dns 설정은 호스트의 설정에 맞게 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="1ba47-121">DNS 동기화는 동적입니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="1ba47-122">호스트에서 변경 되 면 MED-V 작업 영역에서 동적으로 변경 되도록 호스트와 정기적으로 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="1ba47-123">특정 DNS 주소 사용 </strong> -med-v 작업 영역에서 지정 된 대로 특정 dns를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="1ba47-124"><strong>기본 </strong> 및 <strong> 보조 필드에 </strong> 기본 및 보조 DNS 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="1ba47-125">호스트의 <strong> dns 주소 추가 확인란을 선택 </strong> 하 여 호스트를 구성 된 DNS 주소에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ba47-126">DNS 접미사 할당</span><span class="sxs-lookup"><span data-stu-id="1ba47-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="1ba47-127">다음 접미사 할당 </strong> -이 확인란을 선택 하 여 특정 DNS 접미사를 할당 하 고 상자에서 접미사 또는 쉼표로 구분 된 여러 접미사를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="1ba47-128">호스트 접미사 추가 </strong> -호스트 접미사를 DNS 주소에 추가 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ba47-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ba47-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1ba47-129">Related topics</span></span>


[<span data-ttu-id="1ba47-130">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="1ba47-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="1ba47-131">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="1ba47-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





