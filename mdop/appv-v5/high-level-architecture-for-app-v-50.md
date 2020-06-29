---
title: App-V 5.0의 개략적인 아키텍처
description: App-V 5.0의 개략적인 아키텍처
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814556"
---
# <span data-ttu-id="114a2-103">App-V 5.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="114a2-103">High Level Architecture for App-V 5.0</span></span>


<span data-ttu-id="114a2-104">다음 정보를 사용 하 여 Microsoft App-v (Application Virtualization) 5.0 배포를 단순화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

## <span data-ttu-id="114a2-105">아키텍처 개요</span><span class="sxs-lookup"><span data-stu-id="114a2-105">Architecture Overview</span></span>


<span data-ttu-id="114a2-106">일반적인 App-v 5.0 구현에는 다음과 같은 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-106">A typical App-V 5.0 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="114a2-107">요소</span><span class="sxs-lookup"><span data-stu-id="114a2-107">Element</span></span></th>
<th align="left"><span data-ttu-id="114a2-108">추가 정보</span><span class="sxs-lookup"><span data-stu-id="114a2-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114a2-109">App-v 5.0 관리 서버</span><span class="sxs-lookup"><span data-stu-id="114a2-109">App-V 5.0 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="114a2-110">App-v 5.0 관리 서버는 App-v 5.0 인프라에 대 한 전반적인 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-110">The App-V 5.0 Management server provides overall management functionality for the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="114a2-111">또한 환경에 다음 혜택을 제공 하는 관리 서버 인스턴스를 두 개 이상 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="114a2-112">내결함성 및 고가용성 – 서버 중 하나를 사용할 수 없거나 오프 라인일 때 별도의 컴퓨터에 App-v 5.0 관리 서버를 설치 하 고 구성 하는 경우 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.0 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="114a2-113">또한 여러 컴퓨터에 관리 서버를 설치 하 여 App-v 5.0 가용성을 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-113">You can also help increase App-V 5.0 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="114a2-114">이 시나리오에서는 서버 요청이 균형을 유지 하도록 네트워크 부하 분산 장치도 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="114a2-115">확장성 – 부하 분산을 지원 하기 위해 필요에 따라 추가 관리 서버를 추가할 수 있습니다 (예: 로드 균형 조정기 뒤에 여러 개의 서버를 설치할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="114a2-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="114a2-116">App-v 5.0 게시 서버</span><span class="sxs-lookup"><span data-stu-id="114a2-116">App-V 5.0 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="114a2-117">앱-V 5.0 게시 서버는 가상 응용 프로그램 호스팅 및 스트리밍을 위한 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-117">The App-V 5.0 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="114a2-118">게시 서버는 데이터베이스 연결이 필요 하지 않으며 다음 프로토콜을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="114a2-119">HTTP 및 HTTPS</span><span class="sxs-lookup"><span data-stu-id="114a2-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="114a2-120">여러 컴퓨터에 게시 서버를 설치 하 여 앱 V 5.0 가용성을 높일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-120">You can also help increase App-V 5.0 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="114a2-121">또한 서버 요청이 균형을 유지 하도록 네트워크 부하 분산 장치를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114a2-122">App-v 5.0 보고 서버</span><span class="sxs-lookup"><span data-stu-id="114a2-122">App-V 5.0 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="114a2-123">App-v 5.0 보고 서버는 권한이 있는 사용자가 App-v 5.0 인프라를 관리 하는 데 도움이 되는 기존 App-v 5.0 보고서 및 임시 보고서를 실행 하 고 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-123">The App-V 5.0 Reporting server enables authorized users to run and view existing App-V 5.0 reports and ad hoc reports that can help them manage the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="114a2-124">보고 서버는 App-v 5.0 보고 데이터베이스에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-124">The Reporting server requires a connection to the App-V 5.0 reporting database.</span></span> <span data-ttu-id="114a2-125">여러 컴퓨터에 보고 서버를 설치 하 여 앱 V 5.0 가용성을 높일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-125">You can also help increase App-V 5.0 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="114a2-126">또한 서버 요청이 균형을 유지 하도록 네트워크 부하 분산 장치를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="114a2-127">App-v 5.0 클라이언트</span><span class="sxs-lookup"><span data-stu-id="114a2-127">App-V 5.0 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="114a2-128">App-v 5.0 클라이언트는 앱 V 5.0를 사용 하 여 만든 패키지를 대상 컴퓨터에서 실행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-128">The App-V 5.0 client enables packages created using App-V 5.0 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="114a2-129">**참고**  전자 소프트웨어 배포 (ESD)가 포함 된 App-v 5.0를 사용 하는 경우 app-v 5.0 관리 서버를 사용 하는 것이 필요 하지는 않지만 App-v 5.0의 보고 및 스트리밍 기능을 계속 이용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114a2-129">**Note** If you are using App-V 5.0 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.0 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.0.</span></span>

 






## <span data-ttu-id="114a2-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="114a2-130">Related topics</span></span>


[<span data-ttu-id="114a2-131">App-V 5.0 시작</span><span class="sxs-lookup"><span data-stu-id="114a2-131">Getting Started with App-V 5.0</span></span>](getting-started-with-app-v-50--rtm.md)

 

 





