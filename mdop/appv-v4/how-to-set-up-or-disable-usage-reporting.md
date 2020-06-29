---
title: 사용 현황 보고를 설정 또는 사용 중지하는 방법
description: 사용 현황 보고를 설정 또는 사용 중지하는 방법
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816548"
---
# <span data-ttu-id="ecf5e-103">사용 현황 보고를 설정 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="ecf5e-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="ecf5e-104">응용 프로그램 가상화 서버 관리 콘솔에서 다음 절차를 사용 하 여 데이터베이스에 저장 하려는 응용 프로그램 가상화 시스템 사용 정보의 기간 (개월 단위)을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="ecf5e-105">**참고**  사용 정보를 저장 하려면 **공급자 파이프라인** 탭에서 **로그 사용 정보** 확인 확인란을 선택 해야 합니다. 이 탭을 표시 하려면 **공급자 정책 결과** 창에서 공급자 정책을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="ecf5e-106">사용 현황 보고를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="ecf5e-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="ecf5e-107">왼쪽 창에서 Application Virtualization System 노드를 마우스 오른쪽 단추로 클릭 하 고 **시스템 옵션**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="ecf5e-108">**데이터베이스** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="ecf5e-109">**(개월) 사용 기간** 유지 또는 **모든 사용 관리** 라디오 단추를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="ecf5e-110">사용 기간 (월)을 지정 하려면 1 ~ 120 (기본값 6 개월) 사이의 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="ecf5e-111">**모든 사용량 유지**를 선택 하면 지정 된 크기 제한에 도달할 때까지 데이터베이스가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="ecf5e-112">**적용** 또는 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="ecf5e-113">사용 현황 보고 기능을 사용 하지 않으려면</span><span class="sxs-lookup"><span data-stu-id="ecf5e-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="ecf5e-114">**공급자 정책** 노드를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="ecf5e-115">**공급자 정책을** 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="ecf5e-116">**공급자 파이프라인** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="ecf5e-117">**로그 사용 정보** 확인 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="ecf5e-118">**적용** 또는 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf5e-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="ecf5e-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ecf5e-119">Related topics</span></span>


[<span data-ttu-id="ecf5e-120">Server Management Console에서 Application Virtualization 시스템을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="ecf5e-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="ecf5e-121">데이터베이스 크기를 설정 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="ecf5e-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





