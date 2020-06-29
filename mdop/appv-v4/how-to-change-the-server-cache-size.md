---
title: 서버 캐시 크기를 변경하는 방법
description: 서버 캐시 크기를 변경하는 방법
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818028"
---
# <span data-ttu-id="6fb58-103">서버 캐시 크기를 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="6fb58-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="6fb58-104">다음 절차를 사용 하 여 응용 프로그램 가상화 서버 관리 콘솔에서 직접 서버의 캐시 크기를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="6fb58-105">**참고**  캐시 크기를 변경할 수 있지만, 구성에 크기를 변경 해야 하는 경우에는 캐시 크기를 기본값으로 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="6fb58-106">서버 캐시 크기를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="6fb58-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="6fb58-107">왼쪽 창에서 **서버 그룹** 노드를 클릭 하 여 서버 그룹 목록을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="6fb58-108">**결과** 창에서 원하는 서버 그룹을 두 번 클릭 하 여 그룹에 있는 서버 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="6fb58-109">**결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="6fb58-110">**고급** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="6fb58-111">서버 캐시의 **최대 메모리 할당** 필드에 값을 입력 하 고 **경고 메모리 할당** 필드에 임계값 경고 수준에 대 한 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="6fb58-112">**최대 블록 크기** 필드에 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="6fb58-113">이 번호는 서버에서 스트리밍하는 가장 큰 패키지의 최대 블록 크기 보다 크거나 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="6fb58-114">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb58-114">Click **OK**.</span></span>

## <span data-ttu-id="6fb58-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6fb58-115">Related topics</span></span>


[<span data-ttu-id="6fb58-116">서버 포트를 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="6fb58-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="6fb58-117">Server Management Console에서 서버를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="6fb58-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





