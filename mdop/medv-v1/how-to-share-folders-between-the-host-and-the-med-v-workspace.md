---
title: 호스트와 MED-V 작업 영역 간에 폴더를 공유하는 방법
description: 호스트와 MED-V 작업 영역 간에 폴더를 공유하는 방법
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825753"
---
# <span data-ttu-id="95cc9-103">호스트와 MED-V 작업 영역 간에 폴더를 공유하는 방법</span><span class="sxs-lookup"><span data-stu-id="95cc9-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="95cc9-104">호스트와 MED-V 작업 영역 간에 폴더를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="95cc9-105">공유 폴더는 다음에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="95cc9-106">네트워크의 외부 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="95cc9-106">An external computer on the network</span></span>

-   <span data-ttu-id="95cc9-107">호스트 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="95cc9-107">The host computer</span></span>

<span data-ttu-id="95cc9-108">다음 절차에서는 호스트와 MED-V 작업 영역 간에 폴더를 공유 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="95cc9-109">네트워크에 있는 폴더를 공유 하려면</span><span class="sxs-lookup"><span data-stu-id="95cc9-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="95cc9-110">전체 데스크톱 모드에서 MED-V를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="95cc9-111">MED-V 관리의 네트워크 탭에서 **호스트와 다른 IP 주소 사용 (브리지)** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="95cc9-112">호스트 컴퓨터에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="95cc9-113">제어판에서 **네트워크 상태 및 작업 보기**를 클릭 하 고 **네트워크 검색** 을 **On**으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="95cc9-114">시작 메뉴에서 **컴퓨터**를 마우스 오른쪽 단추로 클릭 하 고 **네트워크 드라이브 매핑을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="95cc9-115">**네트워크 드라이브 매핑** 대화 상자의 **drive (드라이브** ) 필드에서 드라이브를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="95cc9-116">**참고**  두 컴퓨터에서 같은 드라이브 문자를 사용 하 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="95cc9-117">**찾아보기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="95cc9-118">**폴더 찾아보기** 대화 상자에서 공유 드라이브를 찾은 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="95cc9-119">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="95cc9-120">MED-V 작업 영역에서 3 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="95cc9-121">호스트 컴퓨터와 같은 드라이브를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="95cc9-122">호스트에 있는 폴더를 공유 하려면</span><span class="sxs-lookup"><span data-stu-id="95cc9-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="95cc9-123">적절 한 사용 권한을 사용 하 여 폴더를 공유 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="95cc9-124">MED-V 작업 영역에서 **내 네트워크 환경** 으로 이동 하 여 공유 폴더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="95cc9-125">MED-V 작업 영역에서 공유 폴더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="95cc9-126">**참고**  호스트와 MED-V 작업 영역 컴퓨터가 모두 동일한 도메인 또는 작업 그룹에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="95cc9-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





