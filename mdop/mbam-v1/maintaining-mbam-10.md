---
title: MBAM 1.0 유지 관리
description: MBAM 1.0 유지 관리
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825773"
---
# <span data-ttu-id="762bb-103">MBAM 1.0 유지 관리</span><span class="sxs-lookup"><span data-stu-id="762bb-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="762bb-104">필요한 계획을 모두 완료 한 다음 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포한 후 엔터프라이즈 BitLocker 암호화 작업을 관리 하는 데 사용 하는 동안 가용성이 높은 방식으로 실행 되도록 MBAM을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="762bb-105">이 섹션의 정보는 MBAM에 대 한 높은 가용성 옵션 및 필요한 경우 MBAM 서버 기능을 이동 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="762bb-106">MBAM 관리 팩</span><span class="sxs-lookup"><span data-stu-id="762bb-106">MBAM Management Pack</span></span>


<span data-ttu-id="762bb-107">MBAM 용 MicrosoftSystemCenterOperationsManager 관리 팩은 Microsoft 다운로드 센터에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="762bb-108">이 관리 팩은 웹 서비스와 데이터베이스 간 연결, 웹사이트의 supportive 웹 서비스 간 운영 호출 등 서버 쪽 인프라의 중요 한 상호 작용을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="762bb-109">또한 데스크톱 클라이언트와 해당 수신 웹 서비스 끝점 간의 요청을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="762bb-110">Microsoft BitLocker 관리 및 모니터링 관리 팩</span><span class="sxs-lookup"><span data-stu-id="762bb-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="762bb-111">MBAM 1.0의 고가용성을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="762bb-112">MBAM은 결함을 허용 하도록 디자인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="762bb-113">서버를 사용할 수 없게 되 면 사용자는 부정적인 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="762bb-114">이 섹션의 정보를 사용 하 여 항상 사용 가능한 MBAM 설치를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="762bb-115">MBAM 1.0에 대한 고가용성</span><span class="sxs-lookup"><span data-stu-id="762bb-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="762bb-116">MBAM 1.0 기능을 다른 서버로 이동</span><span class="sxs-lookup"><span data-stu-id="762bb-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="762bb-117">서버 컴퓨터 간에 MBAM 서버 기능을 이동 해야 하는 경우 생산성 또는 데이터 손실을 방지 하기 위해 따라야 하는 특정 순서 및 필수 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="762bb-118">이 섹션에서는 하나 이상의 MBAM 서버 기능을 다른 컴퓨터로 이동 하기 위해 수행 해야 하는 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="762bb-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="762bb-119">MBAM 1.0 기능을 다른 컴퓨터로 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="762bb-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="762bb-120">MBAM 유지를 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="762bb-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="762bb-121">MBAM 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="762bb-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





