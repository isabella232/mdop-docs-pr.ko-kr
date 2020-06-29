---
title: UE-V 설정 패키지 마이그레이션
description: UE-V 설정 패키지 마이그레이션
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823208"
---
# <span data-ttu-id="cdcc1-103">UE-V 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="cdcc1-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="cdcc1-104">Microsoft UE-V (User Experience Virtualization) 배포 수명 주기에서 새 서버 또는 백업용으로 마이그레이션할 때 사용자 설정 패키지를 재배치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="cdcc1-105">다음과 같은 경우 설정 패키지의 마이그레이션이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="cdcc1-106">기존 서버 하드웨어를 최신 서버로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="cdcc1-107">설정 저장소 위치의 마이그레이션은 랩에서 프로덕션 서버로 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="cdcc1-108">파일 및 폴더를 복사 하기만 해도 보안 설정 및 사용 권한은 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="cdcc1-109">다음의 설명 된 단계에서는 NTFS 권한이 있는 설정 패키지 파일을 새 공유에 올바르게 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="cdcc1-110">새 서버로 마이그레이션할 때 UE-V 설정 패키지를 유지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cdcc1-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="cdcc1-111">다른 서버의 새 위치에서 새 폴더를 만듭니다. 예를 들어 MySettings</span><span class="sxs-lookup"><span data-stu-id="cdcc1-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="cdcc1-112">이전 서버의 이전 폴더 공유에 대해 공유를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="cdcc1-113">명령줄에서 Robocopy를 사용 하 여 기존 설정 패키지를 새 서버로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="cdcc1-114">예:</span><span class="sxs-lookup"><span data-stu-id="cdcc1-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="cdcc1-115">**참고**  복사 진행률을 모니터링 하려면 Trace32와 같은 로그 파일 읽기 프로그램을 사용 하 여 MySettings.txt를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="cdcc1-116">새 공유에 공유 수준 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="cdcc1-117">NTFS 권한은 Robocopy에 의해 설정 된 대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="cdcc1-118">UE-V 에이전트를 실행 하는 컴퓨터에서 SettingsStoragePath 구성 설정을 새 공유의 UNC 경로로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="cdcc1-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cdcc1-119">Related topics</span></span>


[<span data-ttu-id="cdcc1-120">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="cdcc1-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="cdcc1-121">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="cdcc1-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





