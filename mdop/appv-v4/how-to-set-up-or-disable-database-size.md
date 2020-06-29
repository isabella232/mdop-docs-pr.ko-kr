---
title: 데이터베이스 크기를 설정 또는 사용 중지하는 방법
description: 데이터베이스 크기를 설정 또는 사용 중지하는 방법
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816563"
---
# <span data-ttu-id="b8334-103">데이터베이스 크기를 설정 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="b8334-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="b8334-104">응용 프로그램 가상화 서버 관리 콘솔에서 다음 절차를 사용 하 여 데이터베이스에 저장 하려는 응용 프로그램 가상화 시스템 사용량의 크기 (MB)를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="b8334-105">저장 된 데이터의 크기가 지정 된 한도의 95% (상위 워터 마크)에 도달 하면 시스템에서 데이터의 85%가 남아 있는 사용 현황 데이터의 10%를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="b8334-106">패키지 및 응용 프로그램 사용 데이터가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="b8334-107">데이터베이스가 충분히 커지고 상위 워터 마크에 접근 하는 경우에는이 한계에 도달 했음을 알리기 위해 경고 메시지가 SQL Server 로그로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="b8334-108">정리 작업이 보고서의 출력에 영향을 줄 수 있으므로이 경고가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="b8334-109">또한 최대 데이터베이스 크기를 늘리고, 사용 현황 데이터를 유지할 개월 수를 줄이거나, 로깅 수준을 낮출 지 여부를 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="b8334-110">**참고**  사용 현황 보고 및 데이터베이스 정리 기능을 사용 하지 않도록 설정할 수 있도록 **크기 제한 없음** 및 **모든 사용 기간 유지** 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="b8334-111">이러한 항목을 선택 하면 데이터베이스 트랜잭션 로그도 정리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="b8334-112">(모든 커밋된 Microsoft SQL Server 트랜잭션은 데이터베이스 로그에서 제거 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="b8334-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="b8334-113">데이터베이스 크기를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b8334-113">To set up database size</span></span>**

1.  <span data-ttu-id="b8334-114">왼쪽 창에서 Application Virtualization System 노드를 마우스 오른쪽 단추로 클릭 하 고 **시스템 옵션**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="b8334-115">**데이터베이스** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="b8334-116">**최대 데이터베이스 크기 (MB)** 또는 **크기 제한 없음** 라디오 단추를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="b8334-117">데이터베이스 크기를 지정 하도록 선택한 경우에는 512과 4096 MB 사이의 숫자를 입력 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="b8334-118">기본 크기는 1024 MB 이며, 데이터베이스 크기를 늘려야 하는 경우에는 입력할 수 있는 최대 값이 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="b8334-119">**크기 제한을 선택 하지**않으면 디스크 크기 제한에 도달할 때까지 데이터베이스가 증가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="b8334-120">**적용** 또는 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="b8334-121">데이터베이스 크기 제한을 사용 하지 않으려면</span><span class="sxs-lookup"><span data-stu-id="b8334-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="b8334-122">**범위** 창에서 Application Virtualization System 노드를 마우스 오른쪽 단추로 클릭 하 고 **시스템 옵션**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="b8334-123">**데이터베이스** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="b8334-124">**크기 제한 없음** 및 **모든 사용 기간 유지** 라디오 단추를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="b8334-125">**적용** 또는 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8334-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="b8334-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b8334-126">Related topics</span></span>


[<span data-ttu-id="b8334-127">Server Management Console에서 Application Virtualization 시스템을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b8334-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="b8334-128">사용 현황 보고를 설정 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="b8334-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





