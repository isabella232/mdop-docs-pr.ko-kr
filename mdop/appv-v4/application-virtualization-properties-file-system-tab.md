---
title: 응용 프로그램 가상화 속성 파일 시스템 탭
description: 응용 프로그램 가상화 속성 파일 시스템 탭
author: dansimp
ms.assetid: c7d56d36-8c50-4dfc-afee-83dea06376d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57d1f0b340f8fe539c63d439d3c0d883fb322446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822213"
---
# <span data-ttu-id="e066a-103">Application Virtualization 속성: 파일 시스템 탭</span><span class="sxs-lookup"><span data-stu-id="e066a-103">Application Virtualization Properties: File System Tab</span></span>


<span data-ttu-id="e066a-104">**응용 프로그램 가상화 속성** 대화 상자의 **파일 시스템** 탭을 사용 하 여 파일 시스템 설정을 보고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-104">Use the **File System** tab of the **Application Virtualization Properties** dialog box to view and monitor file system settings.</span></span>

<span data-ttu-id="e066a-105">이 탭에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-105">This tab contains the following elements.</span></span>

<a href="" id="client-cache-configuration-settings"></a>**<span data-ttu-id="e066a-106">클라이언트 캐시 구성 설정</span><span class="sxs-lookup"><span data-stu-id="e066a-106">Client Cache Configuration Settings</span></span>**  
<span data-ttu-id="e066a-107">이 섹션에서는 클라이언트 캐시 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-107">This section enables you to configure the client cache settings.</span></span> <span data-ttu-id="e066a-108">다음 라디오 단추 중 하나를 클릭 하 여 캐시 공간을 관리 하는 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-108">Click one of the following radio buttons to choose how to manage the cache space:</span></span>

-   **<span data-ttu-id="e066a-109">최대 캐시 크기 사용</span><span class="sxs-lookup"><span data-stu-id="e066a-109">Use maximum cache size</span></span>**

    <span data-ttu-id="e066a-110">**최대 크기 (mb)** 필드에 100에서 1048576 (1 TB) 사이의 숫자 값을 입력 하 여 캐시의 최대 크기 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-110">Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size in MB of the cache.</span></span> <span data-ttu-id="e066a-111">**예약 된 캐시 크기** 에 표시 되는 값은 사용 중인 캐시의 양을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-111">The value shown in **Reserved Cache Size** indicates the amount of cache in use.</span></span>

-   **<span data-ttu-id="e066a-112">사용 가능한 디스크 공간 임계값</span><span class="sxs-lookup"><span data-stu-id="e066a-112">Use free disk space threshold</span></span>**

    <span data-ttu-id="e066a-113">숫자 값을 입력 하 여 디스크에서 캐시를 사용할 수 있는 빈 디스크 공간 크기 (MB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-113">Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk.</span></span> <span data-ttu-id="e066a-114">이렇게 하면 사용 가능한 디스크 공간 크기가이 한도에 도달할 때까지 캐시가 커질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-114">This allows the cache to grow until the amount of free disk space reaches this limit.</span></span> <span data-ttu-id="e066a-115">**남아 있는 빈 디스크 공간** 에 표시 되는 값은 사용 되지 않은 디스크 공간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-115">The value shown in **Free disk space remaining** indicates how much disk space is unused.</span></span>

<a href="" id="drive-letter"></a>**<span data-ttu-id="e066a-116">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="e066a-116">Drive Letter</span></span>**  
<span data-ttu-id="e066a-117">이 필드는 현재 사용 중인 드라이브를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-117">This field displays the current drive being used.</span></span> <span data-ttu-id="e066a-118">드라이브를 변경 하려면 사용 가능한 드라이브의 드롭다운 목록에서 드라이브 문자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-118">To change the drive, select any drive letter from the drop-down list of available drives.</span></span> <span data-ttu-id="e066a-119">이 설정은 컴퓨터를 다시 부팅할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e066a-119">This setting becomes effective when the computer is rebooted.</span></span>

## <span data-ttu-id="e066a-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e066a-120">Related topics</span></span>


[<span data-ttu-id="e066a-121">Client Management Console: 응용 프로그램 가상화 속성</span><span class="sxs-lookup"><span data-stu-id="e066a-121">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





