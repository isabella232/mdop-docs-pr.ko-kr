---
title: 로그 보고 수준을 변경하고 로그 파일을 다시 설정하는 방법
description: 로그 보고 수준을 변경하고 로그 파일을 다시 설정하는 방법
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818048"
---
# <span data-ttu-id="a8b71-103">로그 보고 수준을 변경하고 로그 파일을 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="a8b71-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="a8b71-104">다음 절차를 사용 하 여 응용 프로그램 가상화 관리 콘솔의 **Application virtualization** 노드에서 로그 보고 수준을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="a8b71-105">로그 파일이 최대 크기에 도달 하면 (기본값은 256 MB) 로그에 다음 쓰기가 발생할 때 재설정이 강제 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="a8b71-106">다시 설정 하면 새 로그 파일이 만들어지고 이전 파일의 이름이 백업으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="a8b71-107">로그 보고 수준을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="a8b71-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="a8b71-108">**Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="a8b71-109">**속성** 대화 상자의 **일반** 탭에 있는 **로그 수준** 드롭다운 목록에서 원하는 로그 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="a8b71-110">**참고**  로깅 수준으로 **Verbose** 를 선택 하면 로그 파일이 매우 빠르게 커집니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="a8b71-111">이렇게 하면 클라이언트 성능이 저하 될 수 있으므로 특정 문제를 진단 하는 데이 로그 수준만 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="a8b71-112">**속성** 대화 상자의 **일반** 탭에 있는 **시스템 로그 수준** 드롭다운 목록에서 원하는 로그 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="a8b71-113">**참고**  **시스템 로그 수준** 설정은 시스템 이벤트 로그에 전송 되는 메시지의 수준을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="a8b71-114">기록 된 메시지는 클라이언트 이벤트 로그에 기록 되는 메시지와 동일 하지만 다른 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="a8b71-115">**확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="a8b71-116">로그 파일을 다시 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="a8b71-116">To reset the log file</span></span>**

1.  <span data-ttu-id="a8b71-117">**Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="a8b71-118">**속성** 대화 상자의 **일반** 탭에서 **로그 다시 설정** 을 클릭 하 여 현재 로그 파일을 백업 하 고 즉시 새 로그 파일을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="a8b71-119">백업 로그 파일은 같은 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="a8b71-120">**확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b71-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="a8b71-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a8b71-121">Related topics</span></span>


[<span data-ttu-id="a8b71-122">Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a8b71-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="a8b71-123">Application Virtualization Client의 사용자 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="a8b71-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





