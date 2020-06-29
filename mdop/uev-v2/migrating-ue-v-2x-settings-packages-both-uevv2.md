---
title: UE-V 2. x 설정 패키지 마이그레이션
description: UE-V 2. x 설정 패키지 마이그레이션
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825518"
---
# <span data-ttu-id="fe4ef-103">UE-V 2. x 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="fe4ef-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="fe4ef-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1 배포의 수명 주기에서 새 서버로 마이그레이션하거나 백업을 수행할 때 사용자 설정 패키지를 재배치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="fe4ef-105">다음과 같은 경우에 설정 패키지를 마이그레이션해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="fe4ef-106">기존 서버 하드웨어를 최신 서버로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="fe4ef-107">설정 저장소 위치의 마이그레이션은 테스트 서버에서 프로덕션 서버로 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="fe4ef-108">단순히 파일 및 폴더를 복사 해도 보안 설정 및 사용 권한은 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="fe4ef-109">다음 단계에서는 설정 패키지를 NTFS 파일 시스템 사용 권한과 함께 새 공유에 올바르게 복사 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="fe4ef-110">새 서버로 마이그레이션할 때 UE-V 2 설정 패키지를 유지 하려면</span><span class="sxs-lookup"><span data-stu-id="fe4ef-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="fe4ef-111">다른 서버의 새 위치에서 MySettings와 같은 새 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="fe4ef-112">이전 서버의 이전 폴더 공유에 대해 공유를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="fe4ef-113">Robocopy를 사용 하 여 기존 설정 패키지를 새 서버에 복사 하려면</span><span class="sxs-lookup"><span data-stu-id="fe4ef-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="fe4ef-114">**참고**  복사 진행률을 모니터링 하려면 Trace32 등의 로그 뷰어로 MySettings.txt를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="fe4ef-115">새 공유에 공유 수준 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="fe4ef-116">NTFS 파일 시스템 권한은 Robocopy에 의해 설정 된 것과 동일 하 게 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="fe4ef-117">UE-V Agent를 실행 하는 컴퓨터에서 **Settingsstoragepath** 구성 설정을 새 공유의 UNC (범용 명명 규칙) 경로로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="fe4ef-118">**Ue-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="fe4ef-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="fe4ef-119">[여기](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="fe4ef-120">**Ue-v 문제가**있나요?</span><span class="sxs-lookup"><span data-stu-id="fe4ef-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="fe4ef-121">[Ue-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4ef-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="fe4ef-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fe4ef-122">Related topics</span></span>


[<span data-ttu-id="fe4ef-123">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="fe4ef-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





