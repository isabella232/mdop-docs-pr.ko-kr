---
title: DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획
description: DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822798"
---
# <span data-ttu-id="838b7-103">DaRT 7.0 복구 이미지를 저장 및 배포하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="838b7-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="838b7-104">Microsoft 진단 및 DaRT (복구 도구 모음) 7 복구 이미지를 저장 하 고 배포 하려는 경우이 섹션의 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="838b7-105">DaRT 복구 이미지를 저장 하 고 배포 하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="838b7-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="838b7-106">다음 방법을 사용 하 여 DaRT 복구 이미지를 저장 하 고 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="838b7-107">사용할 방법을 결정할 때는 각각의 장점과 단점을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="838b7-108">또한 enterprise에서 DaRT를 사용 하는 방법도 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="838b7-109">**참고**  조직에서 두 개 이상의 메서드를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="838b7-110">예를 들어 대부분의 경우 원격 파티션에서 DaRT로 부팅 하 고 최종 사용자 컴퓨터가 네트워크에 연결할 수 없는 경우 USB 플래시 드라이브를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="838b7-111">다음 표에는 조직에서 DaRT를 사용 하는 각 방법의 장점과 단점이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="838b7-112">DaRT로 부팅 하는 방법</span><span class="sxs-lookup"><span data-stu-id="838b7-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="838b7-113">장점</span><span class="sxs-lookup"><span data-stu-id="838b7-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="838b7-114">단점</span><span class="sxs-lookup"><span data-stu-id="838b7-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="838b7-115">CD 또는 DVD에서</span><span class="sxs-lookup"><span data-stu-id="838b7-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-116">MBR (마스터 부트 레코드)이 손상 되 고 하드 디스크에 액세스할 수 없는 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="838b7-117">또한 네트워크 연결이 없는 경우를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="838b7-118">이는 이전 버전의 DaRT 사용자에 게 가장 친숙 하며, <strong> Dart 복구 이미지 마법사에서 직접 CD 또는 DVD를 구울 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="838b7-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-119">CD 또는 DVD에 대 한 액세스 권한이 있는 사용자가 물리적으로 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="838b7-120">UFD (USB 플래시 드라이브)에서</span><span class="sxs-lookup"><span data-stu-id="838b7-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-121">CD 또는 DVD에서 부트할 때와 동일한 이점을 제공 하며 CD 또는 DVD 드라이브가 없는 컴퓨터에도 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-122">DaRT로 부팅 하는 데 UFD를 사용 하기 전에 먼저 UFD의 서식을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="838b7-123">또한 UFD에 대 한 액세스 권한이 있는 다른 사용자가 물리적으로 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="838b7-124">원격 (네트워크) 파티션에서</span><span class="sxs-lookup"><span data-stu-id="838b7-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-125">CD, DVD 또는 UFD 없이 DaRT로 부트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="838b7-126">또한 업데이트할 파일 위치가 하나 밖에 없기 때문에 DaRT를 쉽게 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-127">최종 사용자 컴퓨터가 네트워크에 연결 되어 있지 않은 경우에는 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="838b7-128">최종 사용자가 광범위 하 게 사용할 수 있으며 복구 이미지를 만들 때 추가 보안 고려 사항이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="838b7-129">복구 파티션에서</span><span class="sxs-lookup"><span data-stu-id="838b7-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-130">네트워크 연결이 없는 인스턴스를 포함 하는 CD, DVD 또는 UFD 없이 DaRT로 부팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="838b7-131">또한 Microsoft 끝점 구성 관리자와 같은 자동화 된 배포 도구를 사용 하 여 표준 Windows 이미지 프로세스의 일부로 구현 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="838b7-132">DaRT를 업데이트 하는 경우 한 파티션 (네트워크) 또는 장치 (CD, DVD 또는 UFD)가 아니라 엔터프라이즈의 모든 컴퓨터를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="838b7-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="838b7-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="838b7-133">Related topics</span></span>


[<span data-ttu-id="838b7-134">DaRT 7.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="838b7-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





