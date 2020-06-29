---
title: UE-V 1.0에 대한 설정 저장소 위치 배포
description: UE-V 1.0에 대한 설정 저장소 위치 배포
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826638"
---
# <span data-ttu-id="4f495-103">UE-V 1.0에 대한 설정 저장소 위치 배포</span><span class="sxs-lookup"><span data-stu-id="4f495-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="4f495-104">Microsoft UE-V (User Experience Virtualization) 배포에는 사용자 설정이 설정 패키지 파일에 저장 되어 있는 설정 저장소 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="4f495-105">설정 저장소 위치는 다음 두 가지 방법 중 하나로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="4f495-106">**Active directory home directory** – active directory에서 사용자에 대해 홈 디렉터리가 정의 된 경우 ue-v agent가이 위치를 사용 하 여 설정 위치 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="4f495-107">UE-V agent가 홈 디렉터리의 루트 아래에 있는 사용자 관련 저장소 폴더를 동적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="4f495-108">설정 저장소 위치가 정의 되지 않은 경우 에이전트는 Active Directory의 홈 디렉터리만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="4f495-109">**설정 저장소 공유 만들기** – 설정 저장소 공유는 ue-v 사용자가 액세스할 수 있는 표준 네트워크 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="4f495-110">UE-V 설정 저장소 공유 배포</span><span class="sxs-lookup"><span data-stu-id="4f495-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="4f495-111">설정 저장소 공유를 만들 때 액세스가 필요한 사용자 에게만 액세스를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="4f495-112">필요한 사용 권한은 아래 표에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="4f495-113">UE-V 네트워크 공유를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="4f495-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="4f495-114">UE-V 사용자에 대 한 새 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="4f495-115">중앙에서 찾은 컴퓨터에 UE-V 설정 패키지를 저장할 새 폴더를 만든 다음이 폴더에 대 한 그룹 권한이 있는 UE-V 사용자에 게이를 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="4f495-116">UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="4f495-117">설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="4f495-118">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="4f495-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="4f495-119">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="4f495-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4f495-120">모두</span><span class="sxs-lookup"><span data-stu-id="4f495-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-121">권한 없음</span><span class="sxs-lookup"><span data-stu-id="4f495-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4f495-122">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="4f495-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-123">모든 권한</span><span class="sxs-lookup"><span data-stu-id="4f495-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="4f495-124">설정 저장소 위치 폴더에 대해 다음 NTFS 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="4f495-125">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="4f495-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="4f495-126">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="4f495-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="4f495-127">Folder</span><span class="sxs-lookup"><span data-stu-id="4f495-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4f495-128">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="4f495-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-129">모든 권한</span><span class="sxs-lookup"><span data-stu-id="4f495-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-130">하위 폴더 및 파일만</span><span class="sxs-lookup"><span data-stu-id="4f495-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4f495-131">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="4f495-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-132">폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</span><span class="sxs-lookup"><span data-stu-id="4f495-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f495-133">이 폴더만</span><span class="sxs-lookup"><span data-stu-id="4f495-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="4f495-134">**확인** 을 클릭 하 여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="4f495-135">이 사용 권한 구성에서는 사용자가 설정 저장소에 대 한 폴더를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="4f495-136">UE-V agent는 `settingspackage` 사용자 컨텍스트에서 실행 되는 동안 폴더를 만들고 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="4f495-137">사용자가 해당 폴더에 대 한 모든 권한을 받습니다 `settingspackage` .</span><span class="sxs-lookup"><span data-stu-id="4f495-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="4f495-138">다른 사용자는이 폴더에 대 한 액세스 권한을 상속 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="4f495-139">사용자의 컨텍스트에서 실행 되는 에이전트에 의해 자동으로 수행 되므로 개별 사용자 디렉터리를 만들고 보안 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="4f495-140">**참고**  Windows server가 설정 저장소 공유에 사용 되는 경우 추가 보안을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="4f495-141">로컬 관리자의 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 하도록 UE-V를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="4f495-142">추가 보안을 사용 하도록 설정 하려면 다음을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="4f495-143">"RepositoryOwnerCheckEnabled" 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE** 에 추가 합니다. \\software\\microsoft\\uev\\agent\\configuration.</span><span class="sxs-lookup"><span data-stu-id="4f495-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="4f495-144">레지스트리 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f495-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="4f495-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4f495-145">Related topics</span></span>


[<span data-ttu-id="4f495-146">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="4f495-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="4f495-147">UE-V 1.0에 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="4f495-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="4f495-148">[Ue-v 생성기를 설치 하는](installing-the-ue-v-generator.md) 사용자 환경 가상화 설정 템플릿 및 설정 패키지에 대 한 중앙 저장소 배포</span><span class="sxs-lookup"><span data-stu-id="4f495-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="4f495-149">UE-V 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="4f495-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





