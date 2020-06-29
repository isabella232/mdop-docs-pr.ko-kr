---
title: 캐시 크기 및 드라이브 문자 지정을 변경하는 방법
description: 캐시 크기 및 드라이브 문자 지정을 변경하는 방법
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818038"
---
# <span data-ttu-id="3a757-103">캐시 크기 및 드라이브 문자 지정을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="3a757-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="3a757-104">응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램 가상화** 노드에서 직접 캐시 크기 및 드라이브 문자 지정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="3a757-105">참고</span><span class="sxs-lookup"><span data-stu-id="3a757-105">Note</span></span>**  
<span data-ttu-id="3a757-106">캐시 크기를 설정한 후에는 더 작게 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="3a757-107">캐시 크기를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3a757-107">To change the cache size</span></span>**

1.  <span data-ttu-id="3a757-108">**Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="3a757-109">**속성** 대화 상자에서 **파일 시스템** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="3a757-110">**클라이언트 캐시 구성 설정** 섹션에서 다음 라디오 단추 중 하나를 클릭 하 여 캐시 공간을 관리 하는 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="3a757-111">중요</span><span class="sxs-lookup"><span data-stu-id="3a757-111">Important</span></span>**  
    <span data-ttu-id="3a757-112">**사용 가능한 디스크 공간 임계값** 설정을 선택 하면 입력 하는 값에 의해 캐시 크기가 총 디스크 크기에서 입력 한 빈 디스크 공간 임계값을 뺀 수로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="3a757-113">그런 다음 **최대 캐시 크기 사용** 설정을 사용 하 여 되돌리려는 경우 기존 캐시 크기 보다 큰 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="3a757-114">그렇지 않으면 "새 크기는 기존 캐시 크기 보다 커야 합니다." 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="3a757-115">**확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="3a757-116">드라이브 문자 지정을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3a757-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="3a757-117">**Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="3a757-118">**속성** 대화 상자의 **파일 시스템** 탭에 있는 **사용할 드라이브** 필드에서 사용 가능한 드라이브 문자 드롭다운 목록에서 원하는 드라이브 문자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="3a757-119">이 설정은 컴퓨터를 다시 부팅할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="3a757-120">**확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a757-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="3a757-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3a757-121">Related topics</span></span>


[<span data-ttu-id="3a757-122">Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3a757-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









