---
title: MED-V 로그 보기 및 구성
description: MED-V 로그 보기 및 구성
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823728"
---
# <span data-ttu-id="921c4-103">MED-V 로그 보기 및 구성</span><span class="sxs-lookup"><span data-stu-id="921c4-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="921c4-104">MED-V 문제와 문제를 해결할 때 MED-V 이벤트 로그에 액세스 하는 데 유용 하거나 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="921c4-105">MED-V 관리 도구 키트를 사용 하 여 호스트 컴퓨터 및 게스트 가상 컴퓨터에 대 한 이벤트 뷰어를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="921c4-106">MED-V 관리 도구 키트를 사용 하 여 med-v 이벤트 로그가 MED-V 이벤트를 보고 하는 로깅 수준을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="921c4-107">MED-V 관리 도구 키트를 여는 방법에 대 한 자세한 내용은 [관리 도구 키트를 사용 하 여 Med-v 문제 해결](troubleshooting-med-v-by-using-the-administration-toolkit.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921c4-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="921c4-108">MED-V 이벤트 로그 보기</span><span class="sxs-lookup"><span data-stu-id="921c4-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="921c4-109">**Med-v 관리 툴킷** 창에서 **호스트 이벤트** 를 클릭 하 여 호스트 컴퓨터에 대 한 이벤트 뷰어를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="921c4-110">또는 **게스트 이벤트** 를 클릭 하 여 게스트 가상 컴퓨터에 대 한 이벤트 뷰어를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="921c4-111">이벤트 뷰어가 열리고 MED-V를 배포 하거나 관리할 때 발생할 수 있는 문제를 해결 하는 데 사용할 수 있는 해당 이벤트 로그가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="921c4-112">기본적으로 오류 및 경고만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="921c4-113">특정 이벤트 Id 및 메시지에 대 한 자세한 내용은 [Med-v 이벤트 로그 메시지](med-v-event-log-messages.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921c4-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="921c4-114">**참고**  관리자 권한이 있는 경우 최종 사용자는 이벤트 로그 파일만 게스트에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="921c4-115">호스트 컴퓨터에서 이벤트 뷰어를 수동으로 열려면</span><span class="sxs-lookup"><span data-stu-id="921c4-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="921c4-116">**시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **관리 도구**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="921c4-117">**이벤트 뷰어**를 두 번 클릭 한 다음 **응용 프로그램 및 서비스 로그**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="921c4-118">**Medv**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="921c4-119">MED-V 이벤트 로그 구성</span><span class="sxs-lookup"><span data-stu-id="921c4-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="921c4-120">MED-V 관리 도구 키트에서 해당 옵션 단추를 선택 하 여 MED-V 이벤트 로깅 수준을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="921c4-121">이벤트 로깅에서 오류, 오류, 경고, 오류, 경고 및 정보 메시지를 포함 하는지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="921c4-122">호스트 컴퓨터와 게스트 가상 컴퓨터에 대해 지정 된 이벤트 로깅 수준이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="921c4-123">또한 EventLogLevel 레지스트리 값을 편집 하 여 이벤트 로깅 수준을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="921c4-124">자세한 내용은 [Med-v 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="921c4-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="921c4-125">**참고**  **Med-v 관리 도구 키트** 창에서 지정 하는 수준은 향후 med-v 이벤트 로깅에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="921c4-126">모든 오류, 경고 및 정보 메시지를 캡처하도록 수준을 설정 하면 이벤트 로그가 더 빠르게 채워지기 때문에 이전 이벤트가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="921c4-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="921c4-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="921c4-127">Related topics</span></span>


[<span data-ttu-id="921c4-128">MED-V 작업 영역을 다시 시작하고 다시 설정</span><span class="sxs-lookup"><span data-stu-id="921c4-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="921c4-129">MED-V 작업 영역 구성 보기</span><span class="sxs-lookup"><span data-stu-id="921c4-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





