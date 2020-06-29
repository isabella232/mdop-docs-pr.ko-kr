---
title: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
description: 최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822668"
---
# <span data-ttu-id="bf8c0-103">최종 사용자 컴퓨터에서 크래시 분석기를 실행하는 방법</span><span class="sxs-lookup"><span data-stu-id="bf8c0-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="bf8c0-104">문제가 발생 하는 최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기** 를 실행 하려면 Windows 용 Microsoft 디버깅 도구와 기호 파일이 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="bf8c0-105">Windows 디버깅 도구를 다운로드 하려면 [windows 용 디버깅 도구](https://go.microsoft.com/fwlink/?LinkId=266248)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="bf8c0-106">최종 사용자 컴퓨터에서 충돌 분석기를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="bf8c0-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="bf8c0-107">최종 사용자 컴퓨터의 **진단 및 복구 도구 집합** 창에서 **충돌 분석기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="bf8c0-108">Windows 용 Microsoft 디버깅 도구에 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="bf8c0-109">기호 파일에 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="bf8c0-110">기호 파일에 대 한 자세한 내용은 [충돌 분석기가 기호 파일에 액세스할 수](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md)있도록 하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span></span>

4.  <span data-ttu-id="bf8c0-111">메모리 덤프 파일에 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="bf8c0-112">메모리 덤프 파일의 위치를 확인 하려면 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="bf8c0-113">**시스템 속성** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="bf8c0-114">**시작**을 클릭 하 고 **sysdm.cpl**를 입력 한 다음 **enter 키를**누릅니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="bf8c0-115">**고급** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="bf8c0-116">**시작 및 복구** 영역에서 **설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="bf8c0-117">**시스템 속성** 창에 대 한 액세스 권한이 없으면 Microsoft 진단 및 복구 도구 집합 (DaRT) 10의 **검색** 도구를 사용 하 여 최종 사용자 컴퓨터에서 덤프 파일을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

    <span data-ttu-id="bf8c0-118">**충돌 분석기** 는 메모리 덤프 파일을 검사 하 고 문제의 예상 되는 원인을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="bf8c0-119">오류에 대 한 자세한 정보 (예: 특정 메모리 덤프 메시지 및 설명, 오류 발생 시 로드 되는 드라이버, 분석의 전체 출력)를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="bf8c0-120">적절 한 전략을 식별 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="bf8c0-121">전략에는 DaRT 10의 **컴퓨터 관리** 도구에 있는 **서비스 및 드라이버** 노드를 사용 하 여 오류를 일으킨 장치 드라이버를 사용 하지 않도록 설정 하거나 업데이트 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 10.</span></span>

## <span data-ttu-id="bf8c0-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bf8c0-122">Related topics</span></span>


[<span data-ttu-id="bf8c0-123">크래시 분석기를 사용하여 시스템 오류 진단</span><span class="sxs-lookup"><span data-stu-id="bf8c0-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="bf8c0-124">DaRT 10 작업</span><span class="sxs-lookup"><span data-stu-id="bf8c0-124">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





