---
title: MED-V 클라이언트 도구
description: MED-V 클라이언트 도구
author: dansimp
ms.assetid: ea18d82e-2433-4754-85ac-6eac84bcbb01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e4ae67b8327e41bf5798c1d0d3fcb6253bf3b02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824018"
---
# <span data-ttu-id="2b57e-103">MED-V 클라이언트 도구</span><span class="sxs-lookup"><span data-stu-id="2b57e-103">MED-V Client Tools</span></span>


<span data-ttu-id="2b57e-104">MED-V에는 다음과 같은 클라이언트 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-104">MED-V includes the following client tools:</span></span>

-   [<span data-ttu-id="2b57e-105">파일 전송 도구</span><span class="sxs-lookup"><span data-stu-id="2b57e-105">File Transfer Tool</span></span>](#bkmk-filetransfertool)

-   [<span data-ttu-id="2b57e-106">이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="2b57e-106">Image Downloads</span></span>](#bkmk-imagedownloads)

-   [<span data-ttu-id="2b57e-107">진단</span><span class="sxs-lookup"><span data-stu-id="2b57e-107">Diagnostics</span></span>](#bkmk-diagnostics)

## <a href="" id="bkmk-filetransfertool"></a><span data-ttu-id="2b57e-108">파일 전송 도구</span><span class="sxs-lookup"><span data-stu-id="2b57e-108">File Transfer Tool</span></span>


<span data-ttu-id="2b57e-109">파일 전송 도구를 사용 하 여 MED-V 작업 영역에서 호스트로 파일이 나 폴더를 복사할 수 있으며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-109">The File Transfer Tool can be used to copy files or folders from the MED-V workspace to the host and vice versa.</span></span>

<span data-ttu-id="2b57e-110">**참고**  파일 전송 도구는 MED-V 작업 영역이 실행 되 고 있는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-110">**Note** The File Transfer Tool is enabled only when the MED-V workspace is running.</span></span>

 

**<span data-ttu-id="2b57e-111">현재 실행 중인 MED-V 작업 영역에서 파일 또는 폴더를 복사 하려면</span><span class="sxs-lookup"><span data-stu-id="2b57e-111">To copy files or folders from a MED-V workspace that is currently running</span></span>**

1.  <span data-ttu-id="2b57e-112">알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-112">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="2b57e-113">하위 메뉴에서 **도구**를 가리킨 다음 **파일 전송을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-113">On the submenu, point to **Tools**, and then click **File Transfer**.</span></span>

3.  <span data-ttu-id="2b57e-114">**파일 전송** 도구의 **전송 방향 선택** 필드에서 다음 전송 옵션 중 하나를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-114">In the **File Transfer** tool, in the **Select transfer direction** field, click one of the following transfer options:</span></span>

    -   <span data-ttu-id="2b57e-115">**내 컴퓨터에서 ' 기본 작업 영역 ' 작업 영역으로 복사**-호스트의 파일 또는 폴더를 활성 med-v 작업 영역으로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-115">**Copy from My Computer to 'default workspace' Workspace**—Transfer a file or folder from the host to the active MED-V workspace.</span></span>

    -   <span data-ttu-id="2b57e-116">**' 기본 작업 영역 ' 작업 영역에서 내 컴퓨터로 복사**-활성 med-v 작업 영역의 파일 또는 폴더를 호스트로 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-116">**Copy from 'default workspace' Workspace to My Computer**—Transfer a file or folder from the active MED-V workspace to the host.</span></span>

4.  <span data-ttu-id="2b57e-117">다음 중 하나를 실행 하 여 복사할 파일 또는 폴더를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-117">Select the file or folder to copy by doing one of the following:</span></span>

    -   <span data-ttu-id="2b57e-118">**복사할 파일** 필드에 복사할 파일 또는 폴더가 있는 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-118">In the **File to copy** field, type the full path to the directory where the file or folder to copy is located.</span></span>

    -   <span data-ttu-id="2b57e-119">**찾아보기를** 클릭 하 여 복사할 파일 또는 폴더가 있는 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-119">Click **Browse** to browse the directory where the file or folder to copy is located.</span></span>

5.  <span data-ttu-id="2b57e-120">**폴더 복사** 확인란을 선택 하 여 전체 폴더를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-120">Select the **Copy a folder** check box to copy an entire folder.</span></span>

6.  <span data-ttu-id="2b57e-121">다음 중 하나를 실행 하 여 파일이 전송 되는 대상을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-121">Select the destination where the file is being transferred by doing one of the following:</span></span>

    -   <span data-ttu-id="2b57e-122">**대상** 필드에 파일 또는 폴더가 전송 될 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-122">In the **Destination** field, type the full path of the directory where the file or folder will be transferred.</span></span>

    -   <span data-ttu-id="2b57e-123">**찾아보기를** 클릭 하 여 파일 또는 폴더가 전송 되는 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-123">Click **Browse** to browse to the directory where the file or folder will be transferred.</span></span>

7.  <span data-ttu-id="2b57e-124">**시작**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-124">Click **Start**.</span></span>

    <span data-ttu-id="2b57e-125">파일 전송이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-125">The file transfer begins.</span></span>

## <a href="" id="bkmk-imagedownloads"></a><span data-ttu-id="2b57e-126">이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="2b57e-126">Image Downloads</span></span>


<span data-ttu-id="2b57e-127">MED-V 작업 영역에 새 이미지 업데이트를 사용할 수 있고 MED-V 작업 영역이 활성 상태 이면 사용자는 새 이미지를 다운로드할 준비가 되었음을 나타내는 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-127">When a new image update is available for a MED-V workspace and the MED-V workspace is active, the user receives a message indicating that a new image is ready for download.</span></span>

**<span data-ttu-id="2b57e-128">다운로드할 수 있는 이미지를 보려면</span><span class="sxs-lookup"><span data-stu-id="2b57e-128">To view available images for download</span></span>**

1.  <span data-ttu-id="2b57e-129">알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-129">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="2b57e-130">하위 메뉴에서 **도구**를 가리킨 다음 **이미지 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-130">On the submenu, point to **Tools**, and then click **Image Downloads**.</span></span>

    <span data-ttu-id="2b57e-131">사용할 수 있는 모든 이미지 다운로드가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-131">All available image downloads are displayed.</span></span>

## <a href="" id="bkmk-diagnostics"></a><span data-ttu-id="2b57e-132">진단</span><span class="sxs-lookup"><span data-stu-id="2b57e-132">Diagnostics</span></span>


<span data-ttu-id="2b57e-133">진단 도구는 모든 진단 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-133">The diagnostics tool provides all diagnostic information.</span></span>

**<span data-ttu-id="2b57e-134">진단을 보려면</span><span class="sxs-lookup"><span data-stu-id="2b57e-134">To view diagnostics</span></span>**

1.  <span data-ttu-id="2b57e-135">알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-135">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="2b57e-136">하위 메뉴에서 **도움말**을 가리킨 다음 **med-v 진단을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-136">On the submenu, point to **Help**, and then click **MED-V Diagnostics**.</span></span>

3.  <span data-ttu-id="2b57e-137">**진단** 도구에서 모든 진단 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-137">In the **Diagnostics** tool, review all diagnostic information.</span></span>

<span data-ttu-id="2b57e-138">진단 도구를 사용 하 여 다음 함수를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-138">The following functions can be performed using the diagnostic tool:</span></span>

-   <span data-ttu-id="2b57e-139">진단 로그 수집-진단 로그를 수집 하 여 바탕 화면에 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-139">Gather diagnostic logs—Gather the diagnostic logs, and place them on the desktop.</span></span>

-   <span data-ttu-id="2b57e-140">정책 업데이트 — MED-V 작업 영역 정책은 MED-V 서버에 자동으로 연결 되어 15 분 마다 정책을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-140">Update policy—The MED-V workspace policy automatically connects to the MED-V server to refresh the policy every 15 minutes.</span></span> <span data-ttu-id="2b57e-141">그러나 사용자는이 옵션을 사용 하 여 수동 새로 고침을 즉시 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-141">However, a user can use this option to perform a manual refresh immediately.</span></span>

-   <span data-ttu-id="2b57e-142">진단 모드 사용 또는 사용 안 함-가상 컴퓨터 창을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-142">Enable or Disable diagnostic mode—Display the virtual machine window.</span></span> <span data-ttu-id="2b57e-143">이 함수는 예를 들어, 표시 되지 않는 MED-V 작업 영역 창을 표시 해야 하는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-143">This function is helpful when, for example, you need to see MED-V workspace windows that are not displayed.</span></span>

-   <span data-ttu-id="2b57e-144">이미지 저장소 찾아보기 — 사용 가능한 모든 MED-V 작업 영역 이미지를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="2b57e-144">Browse image store—View all available MED-V workspace images.</span></span>

 

 





