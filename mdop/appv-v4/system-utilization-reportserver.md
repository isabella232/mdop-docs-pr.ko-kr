---
title: 시스템 사용 현황 보고서
description: 시스템 사용 현황 보고서
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815253"
---
# <span data-ttu-id="42e77-103">시스템 사용 현황 보고서</span><span class="sxs-lookup"><span data-stu-id="42e77-103">System Utilization Report</span></span>


<span data-ttu-id="42e77-104">시스템 사용률 보고서를 사용 하 여 총 일일 시스템 사용량을 그래프로 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="42e77-105">이 보고서를 사용 하 여 응용 프로그램 가상화 시스템의 로드를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="42e77-106">이 보고서는 지정 된 서버 또는 서버 그룹에 대해 보고 기간 동안 사용 현황을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="42e77-107">시스템 사용률 보고서에는 다음과 같은 시스템 사용도 그래프로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="42e77-108">요일을 기준으로 사용</span><span class="sxs-lookup"><span data-stu-id="42e77-108">Usage by day of the week</span></span>

-   <span data-ttu-id="42e77-109">일일 시간별 사용량</span><span class="sxs-lookup"><span data-stu-id="42e77-109">Usage by hour of the day</span></span>

<span data-ttu-id="42e77-110">시스템 사용률 보고서에는 특정 사용자의 총 시스템 사용량 및 총 세션 수에 대 한 요약도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="42e77-111">보고서를 만들 때 보고서를 실행할 때 데이터를 수집 하는 데 사용 되는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="42e77-112">보고서는 자동으로 실행 되지 않습니다. 출력 데이터를 생성 하려면이를 명시적으로 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="42e77-113">이 보고서를 실행 하는 데 걸리는 시간은 데이터 저장소에 수집 된 데이터 양에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="42e77-114">보고서를 실행 하 고 출력이 응용 프로그램 가상화 서버 관리 콘솔에 표시 되 면 다음 형식으로 보고서를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="42e77-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="42e77-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="42e77-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="42e77-116">Microsoft Office Excel</span></span>

<span data-ttu-id="42e77-117">**참고**  시스템 사용률 보고서에서 데이터를 표시 하려면 클라이언트에서 보고 한 App-v 서버 이름이 기본 서버 그룹의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="42e77-118">예를 들어 NLB (네트워크 부하 분산 장치)를 사용 하 여 여러 서버를 사용 하는 경우에는 NLB 클러스터 이름을 기본 서버 그룹에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e77-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="42e77-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="42e77-119">Related topics</span></span>


[<span data-ttu-id="42e77-120">보고서를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="42e77-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="42e77-121">보고서를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="42e77-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="42e77-122">보고서를 내보내는 방법</span><span class="sxs-lookup"><span data-stu-id="42e77-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="42e77-123">보고서를 인쇄하는 방법</span><span class="sxs-lookup"><span data-stu-id="42e77-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="42e77-124">보고서를 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="42e77-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





