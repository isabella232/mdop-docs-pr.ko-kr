---
title: UE-V 1.0에 대한 설정 템플릿 카탈로그 배포
description: UE-V 1.0에 대한 설정 템플릿 카탈로그 배포
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826633"
---
# <span data-ttu-id="866f4-103">UE-V 1.0에 대한 설정 템플릿 카탈로그 배포</span><span class="sxs-lookup"><span data-stu-id="866f4-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="866f4-104">사용자 지정 설정 위치 템플릿은 Microsoft UE-V (User Experience Virtualization) 컴퓨터 또는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="866f4-105">컴퓨터의 예약 된 작업은이 위치에서 새 서식 파일이 나 업데이트 된 템플릿을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="866f4-106">이 작업은 매일이 위치를 확인 하 고이 폴더의 서식 파일을 기반으로 동기화 동작을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="866f4-107">마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일은 UE-V agent에 의해 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="866f4-108">이 폴더에서 제거 된 UE-V agent deregisters 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="866f4-109">예약 된 작업이 시스템으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="866f4-110">최소한 네트워크 공유는 Domain Computers 그룹에 대 한 사용 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="866f4-111">또한 저장 된 서식 파일을 관리 하는 관리자에 게 네트워크 공유 폴더에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="866f4-112">사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="866f4-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="866f4-113">UE-V 용 설정 템플릿 카탈로그를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="866f4-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="866f4-114">컴퓨터에서 UE-V 설정 템플릿 카탈로그를 저장할 새 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="866f4-115">설정 템플릿 카탈로그 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="866f4-116">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="866f4-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="866f4-117">권장 권한</span><span class="sxs-lookup"><span data-stu-id="866f4-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="866f4-118">모두</span><span class="sxs-lookup"><span data-stu-id="866f4-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-119">권한 없음</span><span class="sxs-lookup"><span data-stu-id="866f4-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="866f4-120">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="866f4-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-121">읽기 사용 권한 수준</span><span class="sxs-lookup"><span data-stu-id="866f4-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="866f4-122">관리자</span><span class="sxs-lookup"><span data-stu-id="866f4-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-123">읽기/쓰기 권한 수준</span><span class="sxs-lookup"><span data-stu-id="866f4-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="866f4-124">설정 서식 파일 카탈로그 폴더에 대해 다음 NTFS 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="866f4-125">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="866f4-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="866f4-126">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="866f4-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="866f4-127">적용 대상</span><span class="sxs-lookup"><span data-stu-id="866f4-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="866f4-128">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="866f4-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-129">모든 권한</span><span class="sxs-lookup"><span data-stu-id="866f4-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-130">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="866f4-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="866f4-131">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="866f4-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-132">폴더 내용 나열 및 읽기</span><span class="sxs-lookup"><span data-stu-id="866f4-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-133">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="866f4-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="866f4-134">모두</span><span class="sxs-lookup"><span data-stu-id="866f4-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-135">권한 없음</span><span class="sxs-lookup"><span data-stu-id="866f4-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-136">권한 없음</span><span class="sxs-lookup"><span data-stu-id="866f4-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="866f4-137">관리자</span><span class="sxs-lookup"><span data-stu-id="866f4-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-138">모든 권한</span><span class="sxs-lookup"><span data-stu-id="866f4-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="866f4-139">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="866f4-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="866f4-140">**확인** 을 클릭 하 여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="866f4-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="866f4-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="866f4-141">Related topics</span></span>


[<span data-ttu-id="866f4-142">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="866f4-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="866f4-143">UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획</span><span class="sxs-lookup"><span data-stu-id="866f4-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





