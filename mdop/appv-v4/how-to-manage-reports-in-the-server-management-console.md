---
title: Server Management Console에서 보고서를 관리하는 방법
description: Server Management Console에서 보고서를 관리하는 방법
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817143"
---
# <span data-ttu-id="9dede-103">Server Management Console에서 보고서를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="9dede-104">응용 프로그램 가상화 시스템을 효율적으로 관리 하기 위해 Application Virtualization Server Management Console을 사용 하 여 시스템에 대 한 정보를 제공 하는 다양 한 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="9dede-105">이 정보에는 특정 응용 프로그램 또는 모든 응용 프로그램에 대 한 일일 사용량 정보와 시스템 오류 추적이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="9dede-106">참고</span><span class="sxs-lookup"><span data-stu-id="9dede-106">Note</span></span>**  
-   <span data-ttu-id="9dede-107">설치 하는 동안 설치 스크립트는 영어 버전의 보고서 뷰어만 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="9dede-108">보고서 뷰어의 다른 언어로 올바른 정보를 표시 하려면 다음 위치에서 언어 팩을 설치 해야 <https://go.microsoft.com/fwlink/?LinkId=131645> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="9dede-109">서버 관리 콘솔에서 응용 프로그램을 추가 하거나 편집 하는 경우 응용 프로그램 이름과 버전이 OSD 파일에 있는 것과 정확 하 게 일치 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="9dede-110">보고 기능은 보고할 응용 프로그램 사용 현황 데이터를 식별 하는 응용 프로그램 이름 및 버전 데이터 필드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="9dede-111">데이터 필드가 일치 하지 않는 경우 사용 레코드는 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="9dede-112">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="9dede-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="9dede-113">Application Virtualization 보고서 종류</span><span class="sxs-lookup"><span data-stu-id="9dede-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="9dede-114">사용할 수 있는 보고서 형식에 대 한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="9dede-115">보고서를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="9dede-116">보고서를 만들기 위한 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="9dede-117">보고서를 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="9dede-118">보고서를 실행 하는 단계별 프로세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="9dede-119">보고서를 인쇄하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="9dede-120">보고서 인쇄에 대 한 단계별 프로세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="9dede-121">보고서를 내보내는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="9dede-122">보고서 내보내기에 대 한 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="9dede-123">보고서를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="9dede-124">보고서를 삭제 하는 단계별 과정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dede-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="9dede-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9dede-125">Related topics</span></span>


[<span data-ttu-id="9dede-126">응용 프로그램 사용 현황 보고서</span><span class="sxs-lookup"><span data-stu-id="9dede-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="9dede-127">Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dede-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="9dede-128">소프트웨어 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="9dede-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="9dede-129">시스템 오류 보고서</span><span class="sxs-lookup"><span data-stu-id="9dede-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="9dede-130">시스템 사용 현황 보고서</span><span class="sxs-lookup"><span data-stu-id="9dede-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





