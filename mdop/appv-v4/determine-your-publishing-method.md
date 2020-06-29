---
title: 게시 방법 결정
description: 게시 방법 결정
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821678"
---
# <span data-ttu-id="37ebb-103">게시 방법 결정</span><span class="sxs-lookup"><span data-stu-id="37ebb-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="37ebb-104">Application Virtualization Sequencer를 사용 하 여 응용 프로그램을 시퀀싱 한 후 해당 응용 프로그램을 사용자에 게 *게시* 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="37ebb-105">응용 프로그램 게시는 응용 프로그램 가상화 클라이언트가 설치 된 각 컴퓨터에 아이콘, 패키지 정의 정보 및 콘텐츠 원본 위치를 제공 하는 것으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="37ebb-106">다음 표에서는 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 응용 프로그램 가상화를 배포할 때 지원 되는 게시 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37ebb-107">메서드</span><span class="sxs-lookup"><span data-stu-id="37ebb-107">Method</span></span></th>
<th align="left"><span data-ttu-id="37ebb-108">장점</span><span class="sxs-lookup"><span data-stu-id="37ebb-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="37ebb-109">단점</span><span class="sxs-lookup"><span data-stu-id="37ebb-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37ebb-110">독립 실행형 솔루션으로 시퀀싱 하는 동안 Windows Installer 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-111">사용 하기 매우 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-112">패키지가 각 컴퓨터에 로컬로 캐시에 로드 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-113">사용자에 게 표시 되는 아이콘</span><span class="sxs-lookup"><span data-stu-id="37ebb-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-114">기존 소프트웨어 배포와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-115">스트리밍 서버를 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-116">컴퓨터에 있는 패키지 콘텐츠의 위치에는 유연성이 없으며 모든 컴퓨터에 같은 위치가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-117">응용 프로그램을 제거 하려면 프로그램 추가/제거 또는 msiexec만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-118">패키지 업데이트에 필요한 새 버전으로 제거 및 대체</span><span class="sxs-lookup"><span data-stu-id="37ebb-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37ebb-119">시퀀싱 하는 동안 모드, 부하, OVERRIDEURL 명령줄 속성 및 패키지 매니페스트와 함께 사용 하 여 Windows Installer 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-120">유연성을 높이기 위해 간편 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-121">사용자에 게 표시 되는 아이콘</span><span class="sxs-lookup"><span data-stu-id="37ebb-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-122">응용 프로그램이 포함 된 SFT 파일을 스트리밍 원본 위치에 배치 하 고 클라이언트가 해당 위치를 사용 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-123">유연성이 제한 됨-패키지 콘텐츠의 위치만 런타임에 제어 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-124">응용 프로그램을 제거 하려면 프로그램 추가/제거 또는 msiexec만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-125">스트리밍 서버를 사용 하지 않는 경우 패키지 업데이트에 새 버전을 제거 하 고 바꿀 필요가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37ebb-126">SFTMIME 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-127">완전 한 유연성-모든 패키지 관리 기능을 완벽 하 게 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="37ebb-128">ESD 시스템에서 사용할 수 있도록 명령을 스크립트로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-129">각 컴퓨터에서 올바른 순서로 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ebb-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="37ebb-130">명령 언어에 대 한 상세한 이해와 필요한 신중한 계획</span><span class="sxs-lookup"><span data-stu-id="37ebb-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="37ebb-131">이러한 게시 방법을 사용 하는 방법에 대 한 자세한 내용은 [클라이언트에 가상 응용 프로그램을 게시 하는 방법을](how-to-publish-a-virtual-application-on-the-client.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37ebb-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="37ebb-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="37ebb-132">Related topics</span></span>


[<span data-ttu-id="37ebb-133">스트리밍 방법 결정</span><span class="sxs-lookup"><span data-stu-id="37ebb-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="37ebb-134">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="37ebb-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="37ebb-135">전자 소프트웨어 배포 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="37ebb-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="37ebb-136">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="37ebb-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="37ebb-137">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="37ebb-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





