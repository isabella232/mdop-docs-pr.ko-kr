---
title: DaRT 10 복구 이미지를 저장 및 배포하는 방법 계획
description: DaRT 10 복구 이미지를 저장 및 배포하는 방법 계획
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbaa8c4160970de90561f5ff8cedcefd08ca1dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822988"
---
# <span data-ttu-id="cccf1-103">DaRT 10 복구 이미지를 저장 및 배포하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="cccf1-103">Planning How to Save and Deploy the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="cccf1-104">다음 방법을 사용 하 여 Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지를 저장 하 고 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image by using the following methods.</span></span> <span data-ttu-id="cccf1-105">사용할 방법을 결정할 때는 각각의 장점과 단점을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="cccf1-106">또한 인프라 및 지원 직원을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="cccf1-107">소규모 인프라를 사용 하는 경우에는 복구 이미지를 로컬 하드 드라이브에 설치 하는 경우 항상 사용할 수 있기 때문에 이동식 미디어로 DaRT 10을 배포 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-107">If you have a small infrastructure, you might want to deploy DaRT 10 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="cccf1-108">조직에서 AD DS (Active Directory 도메인 서비스)를 사용 하는 경우 Windows DS를 사용 하 여 복구 이미지를 네트워크 서비스로 배포 하는 것이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="cccf1-109">연결 된 컴퓨터는 항상 복구 이미지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="cccf1-110">Windows DS에서 여러 이미지를 배포 하 고 한 곳에서 모두 유지 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="cccf1-111">**참고**  조직에서 두 개 이상의 메서드를 사용 하는 것이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="cccf1-112">예를 들어 대부분의 경우 원격 파티션에서 DaRT로 부팅 하 고 최종 사용자 컴퓨터가 네트워크에 연결할 수 없는 경우 USB 플래시 드라이브를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="cccf1-113">다음 표에는 조직에서 DaRT를 사용 하는 각 방법의 장점과 단점이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cccf1-114">DaRT로 부팅 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cccf1-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="cccf1-115">장점</span><span class="sxs-lookup"><span data-stu-id="cccf1-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="cccf1-116">단점</span><span class="sxs-lookup"><span data-stu-id="cccf1-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cccf1-117">이동식 미디어</span><span class="sxs-lookup"><span data-stu-id="cccf1-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="cccf1-118">복구 이미지는 지원 직원이이를 불안정 한 컴퓨터로 복구 도구를 사용할 수 있도록 CD, DVD 또는 USB 드라이브에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-119">MBR (마스터 부트 레코드)이 손상 되 고 하드 디스크에 액세스할 수 없고 네트워크 연결이 없는 경우를 지원 하는 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="cccf1-120">여러 도구를 사용 하 여 다양 한 지원 수준을 제공 하는 다양 한 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="cccf1-121">이동식 미디어에 복구 이미지를 구울 수 있는 기본 제공 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-122">지원 직원이 물리적으로 최종 사용자 컴퓨터를 사용 하 여 DaRT로 부팅 하도록 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="cccf1-123">32 비트 및 64 비트 컴퓨터에 대해 서로 다른 구성을 사용 하 여 여러 미디어를 만들려면 시간과 유지 관리가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cccf1-124">원격 (네트워크) 파티션에서</span><span class="sxs-lookup"><span data-stu-id="cccf1-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="cccf1-125">복구 이미지는 사용자 또는 지원 직원이 필요할 때 컴퓨터에 스트리밍할 수 있도록 하는 windows DS (Windows 배포 서비스)와 같은 네트워크 부팅 서버에서 호스팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-126">네트워크 부팅 서버에 대 한 액세스 권한이 있는 모든 컴퓨터에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="cccf1-127">복구 이미지는 중앙 서버에서 호스팅되므로 중앙 집중식 업데이트를 가능 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="cccf1-128">중앙 집중화 된 지원 센터 직원은 원격 연결을 사용 하 여 복구를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="cccf1-129">클라이언트에 로컬 저장소 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="cccf1-130">특정 지원 수준에 대 한 다양 한 도구를 사용 하 여 여러 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-131">일반 사용자가 전체 운영 체제 이미징 프로세스가 아닌 DaRT 복구 이미지만 시작할 수 있도록 Windows DS 인프라를 보호 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="cccf1-132">최종 사용자 컴퓨터가 런타임에 네트워크에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="cccf1-133">네트워크를 통해 복구 이미지를 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cccf1-134">로컬 하드 드라이브의 복구 파티션에서</span><span class="sxs-lookup"><span data-stu-id="cccf1-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="cccf1-135">복구 이미지는 수동으로 또는 System Center Configuration Manager와 같은 전자 소프트웨어 배포 시스템을 사용 하 여 로컬 하드 드라이브에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-136">복구 이미지는 컴퓨터에 미리 준비 되어 있으므로 항상 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="cccf1-137">중앙 집중화 된 지원 센터 직원은 원격 연결을 사용 하 여 지원을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="cccf1-138">복구 이미지는 중앙에서 관리 되 고 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="cccf1-139">Windows BitLocker 드라이브 암호화로 보호 되는 컴퓨터의 추가 복구 키 요청이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cccf1-140">로컬 저장소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="cccf1-141">복구 이미지 배치에 대 한 암호화 되지 않은 전용 파티션을 사용할 경우 실패 한 부팅 파티션의 위험을 줄이는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="cccf1-142">DaRT를 업데이트 하는 경우 한 파티션 (네트워크의 경우) 또는 이동식 장치에 대 한 것이 아니라 엔터프라이즈의 모든 컴퓨터를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="cccf1-143">BitLocker를 사용 하도록 설정한 후 복구 이미지를 배포 하는 경우 추가 고려 사항이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cccf1-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cccf1-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cccf1-144">Related topics</span></span>


[<span data-ttu-id="cccf1-145">DaRT 10 배포 계획</span><span class="sxs-lookup"><span data-stu-id="cccf1-145">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





