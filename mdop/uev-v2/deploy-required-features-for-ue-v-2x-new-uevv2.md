---
title: UE-V 2.x에 대한 필수 기능 배포
description: UE-V 2.x에 대한 필수 기능 배포
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824668"
---
# <span data-ttu-id="e4d7d-103">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="e4d7d-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="e4d7d-104">모든 Microsoft UE-V (사용자 환경 가상화) 2.0, 2.1 및 2.1 SP1 배포에는 다음 기능이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="e4d7d-105">최종 사용자가 액세스할 수 있는 [설정 저장소 위치를 배포](#ssl) 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="e4d7d-106">사용자 설정을 저장 하 고 검색 하는 표준 네트워크 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="e4d7d-107">UE-V에 대 한 구성 방법 선택</span><span class="sxs-lookup"><span data-stu-id="e4d7d-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="e4d7d-108">UE-V는 그룹 정책, 구성 관리자 또는 Windows 관리 인프라 및 Powershell을 비롯 한 일반적인 관리 도구를 사용 하 여 배포 및 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="e4d7d-109">설정을 동기화 하는 모든 컴퓨터에 설치할 [Ue-v agent를 배포](#agent) 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="e4d7d-110">이는 등록 된 응용 프로그램 및 운영 체제를 모니터링 하 여 설정을 변경 하 고 컴퓨터 간에 해당 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="e4d7d-111">이 섹션의 항목에서는 이러한 기능을 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="e4d7d-112">UE-V 설정 저장소 위치 배포</span><span class="sxs-lookup"><span data-stu-id="e4d7d-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="e4d7d-113">UE-V를 사용 하려면 설정 패키지 파일에 사용자 설정을 저장할 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="e4d7d-114">다음 방법 중 하나를 수행 하 여이 설정 저장소 위치를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="e4d7d-115">자신만의 설정 저장소 위치 만들기</span><span class="sxs-lookup"><span data-stu-id="e4d7d-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="e4d7d-116">설정 저장소 위치에 기존 Active Directory 사용</span><span class="sxs-lookup"><span data-stu-id="e4d7d-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="e4d7d-117">설정 저장소 위치를 만들지 않으면 UE-V Agent가 기본적으로 AD (Active Directory)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="e4d7d-118">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-118">Note</span></span>**  
<span data-ttu-id="e4d7d-119">[성능 및 용량 계획](https://technet.microsoft.com/library/dn458932.aspx#capacity) 의 일환으로 네트워크 지연 문제를 줄이기 위해 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="e4d7d-120">설정 저장소 위치에 대해 사용자 당 20mb의 디스크 공간을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="e4d7d-121">UE-V 설정 저장소 위치 만들기</span><span class="sxs-lookup"><span data-stu-id="e4d7d-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="e4d7d-122">설정 저장소 위치를 정의 하기 전에 공유에 설정을 저장 하는 사용자에 대 한 읽기/쓰기 권한을 사용 하 여 루트 디렉터리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="e4d7d-123">UE-V Agent는이 루트 디렉터리 아래에 사용자 관련 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="e4d7d-124">설정 저장소 위치는 다음 방법 중 하나를 사용 하 여 구성할 수 있는 SettingsStoragePath 구성 옵션을 설정 하 여 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="e4d7d-125">명령줄 매개 변수 또는 일괄 처리 스크립트를 통해 [Ue-v 에이전트를 배포](#agent) 하는 경우</span><span class="sxs-lookup"><span data-stu-id="e4d7d-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="e4d7d-126">[그룹 정책](https://technet.microsoft.com/library/dn458893.aspx) 설정</span><span class="sxs-lookup"><span data-stu-id="e4d7d-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="e4d7d-127">UE-V 용 [System Center 구성 팩](https://technet.microsoft.com/library/dn458917.aspx) 사용</span><span class="sxs-lookup"><span data-stu-id="e4d7d-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="e4d7d-128">UE-V 에이전트를 설치한 후 [Windows PowerShell 또는 WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx) 를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="e4d7d-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="e4d7d-129">경로는 서버 및 공유의 UNC (범용 명명 규칙) 경로에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="e4d7d-130">예를 **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="e4d7d-131">이 구성 옵션은 특정 동기화 시나리오를 사용 하도록 설정 하는 변수 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="e4d7d-132">예를 들어 `%username%\%computername%` 다음과 같은 시나리오에서 변수를 사용 하 여 최종 사용자 설정 환경을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="e4d7d-133">엔터프라이즈에서 여러 물리적 컴퓨터를 사용 하는 최종 사용자</span><span class="sxs-lookup"><span data-stu-id="e4d7d-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="e4d7d-134">여러 최종 사용자가 사용 하는 Enterprise 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="e4d7d-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="e4d7d-135">UE-V Agent는 `SettingsPackages` **Settingsstoragepath**의 구성 설정을 기반으로 명명 된 숨겨진 시스템 폴더를 사용 하 여 사용자 관련 설정 저장소 경로를 동적으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="e4d7d-136">에이전트는 등록 된 UE-V 설정 위치 템플릿에서 정의한 대로이 위치에 대 한 설정을 읽고 씁니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="e4d7d-137">**Ue-v 설정은 "마지막 쓰기 wins" 규칙에 따라 결정 됩니다.** 설정 저장소 위치가 여러 관리 컴퓨터를 사용 하는 사용자의 경우, 한 UE-V Agent가 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="e4d7d-138">마지막으로 작성 한 설정 및 값은 다음 에이전트가 설정 저장소 위치에서 읽을 때 적용 되는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="e4d7d-139">**설정 저장소 위치 배포:** 다음 단계에 따라 기존 Active Directory 서비스를 사용 하는 대신 설정 저장소 위치를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="e4d7d-140">아래 표에 표시 된 것 처럼 설정 저장소 공유에 대 한 액세스 권한을 필요로 하는 사용자에 게 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="e4d7d-141">UE-V 네트워크 공유를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="e4d7d-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="e4d7d-142">UE-V 사용자에 대 한 새 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="e4d7d-143">UE-V 설정 패키지를 저장 하는 중앙 컴퓨터에서 새 폴더를 만든 다음이 폴더에 대 한 그룹 사용 권한을 사용 하 여 UE-V 사용자에 게 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="e4d7d-144">UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="e4d7d-145">설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준 서버 메시지 블록) 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="e4d7d-146">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="e4d7d-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e4d7d-147">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="e4d7d-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e4d7d-148">모두</span><span class="sxs-lookup"><span data-stu-id="e4d7d-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-149">권한 없음</span><span class="sxs-lookup"><span data-stu-id="e4d7d-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e4d7d-150">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="e4d7d-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-151">모든 권한</span><span class="sxs-lookup"><span data-stu-id="e4d7d-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="e4d7d-152">설정 저장소 위치 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="e4d7d-153">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="e4d7d-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e4d7d-154">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="e4d7d-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e4d7d-155">Folder</span><span class="sxs-lookup"><span data-stu-id="e4d7d-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e4d7d-156">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="e4d7d-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-157">모든 권한</span><span class="sxs-lookup"><span data-stu-id="e4d7d-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-158">하위 폴더 및 파일만</span><span class="sxs-lookup"><span data-stu-id="e4d7d-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e4d7d-159">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="e4d7d-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-160">폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</span><span class="sxs-lookup"><span data-stu-id="e4d7d-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e4d7d-161">이 폴더만</span><span class="sxs-lookup"><span data-stu-id="e4d7d-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="e4d7d-162">이 구성을 사용 하면 UE-V Agent가 사용자 컨텍스트에서 실행 되는 동안 Settingspackage 폴더를 만들고 보호 하며, 설정 저장소에 대 한 폴더를 만들 수 있는 권한을 각 사용자에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="e4d7d-163">다른 사용자가 액세스할 수 없는 동안 사용자는 자신의 Settingspackage 폴더에 대 한 모든 권한을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="e4d7d-164">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-164">Note</span></span>**  
<span data-ttu-id="e4d7d-165">Windows Server 운영 체제를 실행 하는 컴퓨터에서 설정 저장소 공유를 만드는 경우 UE-V를 구성 하 여 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="e4d7d-166">이 추가 보안을 사용 하도록 설정 하려면 Windows Server 레지스트리 편집기에서 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="e4d7d-167">**"RepositoryOwnerCheckEnabled"** 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="e4d7d-168">레지스트리 키 값을 *1*로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="e4d7d-169">UE-V를 사용 하 여 Active Directory/V 2. x 포함</span><span class="sxs-lookup"><span data-stu-id="e4d7d-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="e4d7d-170">설정 저장소 위치가 달리 정의 되지 않은 경우 UE-V Agent가 기본적으로 Active Directory (AD)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="e4d7d-171">이러한 경우 UE-V Agent가 각 사용자의 AD home 디렉터리 아래에서 동적으로 설정 저장소 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="e4d7d-172">그러나 AD에서 사용자 지정 디렉터리 설정이 구성 되어 있으면 해당 디렉터리가 대신 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="e4d7d-173">UE-V 2. x에 대 한 구성 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="e4d7d-174">이는 UE-V 에이전트를 배포 하는 데 사용 하는 구성 방법 이므로 배포 후 UE-V를 관리 하는 데 사용할 구성 방법을 알아내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="e4d7d-175">일반적으로이는 Windows PowerShell 또는 Configuration Manager와 같이 환경에서 이미 사용 하는 구성 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="e4d7d-176">UE-V 에이전트를 설치 하기 전이나 설치한 후에는 사용 하는 구성 방법에 따라 UE-V를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="e4d7d-177">[그룹 정책](https://technet.microsoft.com/library/dn458893.aspx)**:** 기존 그룹 정책 인프라를 사용 하 여 ue-v 에이전트 배포 전 또는 후에 ue-v를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="e4d7d-178">UE-V 그룹 정책 ADMX 서식 파일은 일반적인 UE-V 에이전트 구성 옵션의 중앙 관리를 가능 하 게 하며 UE-V 동기화를 구성 하는 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="e4d7d-179">**Ue-v 그룹 정책 ADMX 템플릿 설치:** UE-V 용 그룹 정책 ADMX 템플릿은 UE-V 에이전트에 대 한 동기화 설정을 구성 하 고 기존 그룹 정책 인프라를 사용 하 여 일반적인 UE-V Agent 구성 설정의 중앙 관리를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="e4d7d-180">그룹 정책 개체를 배포 하는 도메인 컨트롤러에 대해 지원 되는 운영 체제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="e4d7d-181">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4d7d-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="e4d7d-182">Windows Server 2012 및 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e4d7d-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="e4d7d-183">[구성 관리자](https://technet.microsoft.com/library/dn458917.aspx)**:** ue-v 구성 팩을 사용 하면 System Center configuration Manager 2012 SP1 이상 버전의 규정 준수 설정 기능을 통해 ue-v 및 Configuration manager가 설치 된 사이트에서 일관 된 구성을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="e4d7d-184">[Windows powershell 및 wmi](https://technet.microsoft.com/library/dn458937.aspx)**:** windows powershell 및 wmi (windows Management Instrumentation)에 대해 스크립팅된 명령을 사용 하 여 ue-v 에이전트를 설치한 후 구성을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="e4d7d-185">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-185">Note</span></span>**  
    <span data-ttu-id="e4d7d-186">레지스트리를 수정 하면 데이터가 손실 되거나 컴퓨터가 응답 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="e4d7d-187">다른 구성 메서드를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="e4d7d-188">**명령줄 또는 배치 스크립트 설치:** [Ue-v 에이전트를 배포할](#agent) 때 사용 되는 매개 변수는 여러 ue-v 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="e4d7d-189">System Center 2012 구성 관리자와 같은 전자 소프트웨어 배포 시스템에서는 이러한 매개 변수를 사용 하 여 UE-V 에이전트 소프트웨어를 배포 하 고 설치할 때 해당 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="e4d7d-190">UE-V 2. x 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="e4d7d-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="e4d7d-191">UE-V Agent는 UE-V 배포의 핵심 이며 UE-V를 사용 하 여 응용 프로그램 및 Windows 설정을 동기화 하는 각 컴퓨터에서 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="e4d7d-192">**Ue-v 에이전트 설치 파일:** AgentSetup.exe 단일 설치 파일은 32 비트 및 64 비트 운영 체제에 모두 UE-V Agent를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="e4d7d-193">또한 AgentSetupx86.msi 또는 AgentSetupx64.msi 아키텍처 관련 Windows Installer 파일이 제공 되며,이는 크기가 작기 때문에 에이전트 배포를 단순화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="e4d7d-194">Windows Installer 설치에도 [AgentSetup.exe 설치 관리자의 명령줄 매개 변수가](#params) 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="e4d7d-195">중요</span><span class="sxs-lookup"><span data-stu-id="e4d7d-195">Important</span></span>**  
<span data-ttu-id="e4d7d-196">UE-V 에이전트 설치 또는 제거 중에 AgentSetup.exe 파일 또는 AgentSetup &lt; 아치 &gt; .msi 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="e4d7d-197">UE-V 에이전트를 설치 하는 데 사용 된 UE-V Agent를 제거 하려면 같은 파일을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="e4d7d-198">UE-V 에이전트를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="e4d7d-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="e4d7d-199">다음 메서드를 사용 하 여 UE-V 에이전트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="e4d7d-200">Windows Installer (.msi) 파일을 설치할 수 있는 구성 관리자 등의 ESD (전자 소프트웨어 배포) 솔루션 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="e4d7d-201">공유에 중앙에 저장 된 Windows Installer (.msi) 파일을 참조 하는 설치 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="e4d7d-202">컴퓨터에서 수동으로 실행 하는 설치 프로그램</span><span class="sxs-lookup"><span data-stu-id="e4d7d-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="e4d7d-203">네트워크 공유에서 UE-V Agent를 배포 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="e4d7d-204">네트워크 공유에서 UE-V Agent를 설치 하 고 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="e4d7d-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="e4d7d-205">사용자가 읽기 권한을 가지는 네트워크 공유에 AgentSetup.exe UE-V 에이전트 설치 파일을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="e4d7d-206">UE-V Agent를 설치 하는 사용자 컴퓨터에 스크립트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="e4d7d-207">스크립트는 설정 저장소 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="e4d7d-208">**배포 옵션:** UE-V 에이전트를 설치할 때 올바른 변수 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="e4d7d-209">다음 표에서는 AgentSetup.exe 또는 Windows Installer (.msi) 파일을 사용 하는 배포 옵션의 예를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e4d7d-210">배포 유형</span><span class="sxs-lookup"><span data-stu-id="e4d7d-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e4d7d-211">배포 설명</span><span class="sxs-lookup"><span data-stu-id="e4d7d-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e4d7d-212">예</span><span class="sxs-lookup"><span data-stu-id="e4d7d-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-213">명령 프롬프트</span><span class="sxs-lookup"><span data-stu-id="e4d7d-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-214">명령 프롬프트에서 UE-V Agent를 설치 하는 경우 <em> % ^ username% </em> 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="e4d7d-215">설정 저장소 경로의 공간 때문에 인용 부호가 필요한 경우 배포용 배치 스크립트 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-216">일괄 처리 스크립트</span><span class="sxs-lookup"><span data-stu-id="e4d7d-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-217">배치 스크립트 파일에서 UE-V 에이전트를 설치 하는 경우 <em> %% username%% </em> 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="e4d7d-218">이 설치 방법을 사용 하는 경우%% 문자로 변수를 이스케이프 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="e4d7d-219">이 문자를 사용 하지 않으면 스크립트가 <em> 런타임 대신 설치 시 사용자 이름 변수를 확장 하 여 </em> ue-v가 모든 사용자에 대해 단일 설정 저장소 위치를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4d7d-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-221">Windows PowerShell 프롬프트 또는 Windows PowerShell 스크립트에서 UE-V Agent를 설치 하는 경우 <em> % username% </em> 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-222">전자 소프트웨어 배포 (예: Configuration Manager 소프트웨어 배포 배포)</span><span class="sxs-lookup"><span data-stu-id="e4d7d-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-223">Configuration Manager를 사용 하 여 UE-V 에이전트를 설치 하는 경우 <em> ^% username ^% </em> 변수 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e4d7d-224">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-224">Note</span></span>**  
<span data-ttu-id="e4d7d-225">UE-V 에이전트를 설치 하려면 관리자 권한이 필요 하며, 컴퓨터를 다시 시작 해야 UE-V Agent를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="e4d7d-226">UE-V 에이전트 배포의 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4d7d-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="e4d7d-227">UE-V 에이전트의 명령줄 매개 변수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e4d7d-228">명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4d7d-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e4d7d-229">정의</span><span class="sxs-lookup"><span data-stu-id="e4d7d-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e4d7d-230">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-231">/help 또는/h 또는/?</span><span class="sxs-lookup"><span data-stu-id="e4d7d-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-232">AgentSetup.exe 사용 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="e4d7d-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-234">설정이 저장 되는 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="e4d7d-235">중요</span><span class="sxs-lookup"><span data-stu-id="e4d7d-235">Important</span></span></strong><br/><p><span data-ttu-id="e4d7d-236">UE-V 2.1 및 UE-V 2.1 SP1에서 SettingsStoragePath를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="e4d7d-237">AdHomePath 문자열을 설정 하 여 사용자&#39;s Active Directory home path를 사용 하도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="e4d7d-238">예를 들면 <code>SettingsStoragePath = \share\path|AdHomePath</code>입니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="e4d7d-239">UE-V 2.0에서 Active Directory home 경로를 대신 사용 하도록 SettingsStoragePath를 비워 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e4d7d-240">% username% 또는% computername% 환경 변수를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="e4d7d-241">스크립팅에는 이스케이프 된 변수가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="e4d7d-242">기본값 </strong> : &lt; 없음&gt;</span><span class="sxs-lookup"><span data-stu-id="e4d7d-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="e4d7d-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-244">설치 하는 동안 레지스트리에서 SettingsStoragePath 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-245">명령 프롬프트에서 다음 예제를 입력 하 여 UE-V가 특정 UNC 대신 Active Directory home 경로를 사용 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="e4d7d-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-247">새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-248">사용자 지정 설정 위치 서식 파일에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="e4d7d-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-250">설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-251">True | 해제</span><span class="sxs-lookup"><span data-stu-id="e4d7d-251">True | False</span></span></p>
<p><strong><span data-ttu-id="e4d7d-252">기본값 </strong> : True</span><span class="sxs-lookup"><span data-stu-id="e4d7d-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-253">Powerschool</span><span class="sxs-lookup"><span data-stu-id="e4d7d-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-254">사용할 동기화 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-255">SyncProvider | 않아야</span><span class="sxs-lookup"><span data-stu-id="e4d7d-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="e4d7d-256">기본값 </strong> : syncprovider</span><span class="sxs-lookup"><span data-stu-id="e4d7d-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="e4d7d-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-258">설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e4d7d-259">기본값 </strong> : 2000 밀리초</span><span class="sxs-lookup"><span data-stu-id="e4d7d-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="e4d7d-260">(2 초까지 대기)</span><span class="sxs-lookup"><span data-stu-id="e4d7d-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="e4d7d-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-262">UE-V 동기화를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-263">True | 해제</span><span class="sxs-lookup"><span data-stu-id="e4d7d-263">True | False</span></span></p>
<p><strong><span data-ttu-id="e4d7d-264">기본값 </strong> : True</span><span class="sxs-lookup"><span data-stu-id="e4d7d-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e4d7d-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-266">UE-V Agent가 해당 파일이 임계값을 초과 하는 것으로 보고할 때 설정 패키지 파일 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-267">&lt;크기&gt;</span><span class="sxs-lookup"><span data-stu-id="e4d7d-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="e4d7d-268">기본값 </strong> : 없음 (경고 임계값 없음)</span><span class="sxs-lookup"><span data-stu-id="e4d7d-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="e4d7d-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-270">사용자 환경 개선 프로그램의 참여에 대 한 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="e4d7d-271">True로 설정 <strong> 하면 </strong> 설치 관리자 정보가 Microsoft 사용자 환경 개선 프로그램 사이트에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="e4d7d-272">False로 설정 <strong> </strong> 된 경우 정보는 업로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-273">True | 해제</span><span class="sxs-lookup"><span data-stu-id="e4d7d-273">True | False</span></span></p>
<p><strong><span data-ttu-id="e4d7d-274">기본값 </strong> : False</span><span class="sxs-lookup"><span data-stu-id="e4d7d-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-275">NoRestart</span><span class="sxs-lookup"><span data-stu-id="e4d7d-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-276">UE-V Agent가 설치 된 후 컴퓨터를 다시 시작 하는 지연을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="e4d7d-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-278">UE-V 에이전트 또는 UE-V 생성기에 대해 다른 설치 폴더를 설정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="e4d7d-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-280">설치 프로그램이 Microsoft Update 프로그램에 포함 되는 옵션을 허용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4d7d-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="e4d7d-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-282">UE-V를 자동으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="e4d7d-283"><strong> </strong> Ue-v를 자동으로 설치 하 고 사용자가 ue-v 라이선스 조건을 허용 하는 요구 사항을 무시 하려면이를 True로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="e4d7d-284">False로 설정 <strong> </strong> 되거나 비어 있는 경우 사용자에 게 오류 메시지가 발생 하 고 ue-v가 설치 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="e4d7d-285">중요</span><span class="sxs-lookup"><span data-stu-id="e4d7d-285">Important</span></span></strong><br/><p><span data-ttu-id="e4d7d-286">이 매개 변수는 UE-V를 자동으로 설치 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4d7d-287">NORESTART</span><span class="sxs-lookup"><span data-stu-id="e4d7d-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4d7d-288">UE-V Agent가 설치 된 후 필수 다시 시작을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e4d7d-289">UE-V 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="e4d7d-289">Update the UE-V Agent</span></span>

<span data-ttu-id="e4d7d-290">UE-V 에이전트 소프트웨어에 대 한 업데이트는 Microsoft Update를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="e4d7d-291">ESD (엔터프라이즈 소프트웨어 배포) 인프라 시스템을 사용 하 여 UE-V 에이전트 업데이트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="e4d7d-292">UE-V 에이전트 업그레이드 중에 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치 템플릿의 기본 그룹을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="e4d7d-293">UE-V 2. x 에이전트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="e4d7d-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="e4d7d-294">UE-V 2. x 에이전트는 여러 가지 새로운 기능을 도입 하 고 에이전트가 설정 저장소 공유에 콘텐츠를 업로드 하는 방법과 시기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="e4d7d-295">업그레이드 프로세스는 이러한 변경을 자동화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="e4d7d-296">UE-V Agent를 업그레이드 하려면 사용자 컴퓨터에서 UE-V Agent 설치 패키지 (AgentSetup.exe, AgentSetupx86.msi 또는 AgentSetupx64.msi)를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="e4d7d-297">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-297">Note</span></span>**  
<span data-ttu-id="e4d7d-298">UE-V Agent를 업그레이드 하는 경우 이전 UE-V 에이전트를 설치 하는 동일한 설치 관리자 유형 (.exe 파일 또는 .msi 패킷)을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="e4d7d-299">예를 들어 UE-V 1.0 AgentSetup.exe를 사용 하 여 AgentSetup.exe를 사용 하 여 설치한 UE-V 에이전트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="e4d7d-300">에이전트 설정 프로그램이 실행 될 때 다음 구성이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="e4d7d-301">설정 저장소 경로</span><span class="sxs-lookup"><span data-stu-id="e4d7d-301">Settings storage path</span></span>

-   <span data-ttu-id="e4d7d-302">레지스트리 설정</span><span class="sxs-lookup"><span data-stu-id="e4d7d-302">Registry settings</span></span>

-   <span data-ttu-id="e4d7d-303">예약 된 작업 (간격 설정이 기본값으로 다시 설정 됨)</span><span class="sxs-lookup"><span data-stu-id="e4d7d-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="e4d7d-304">참고</span><span class="sxs-lookup"><span data-stu-id="e4d7d-304">Note</span></span>**  
<span data-ttu-id="e4d7d-305">Ue-v 1.0 에이전트에 등록 되어 있는 UE-V 2. x 설정 위치 템플릿이 있는 컴퓨터는 Windows 이벤트 로그에 오류를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="e4d7d-306">Microsoft System Center 2012 구성 관리자 또는 다른 엔터프라이즈 소프트웨어 배포 도구를 사용 하 여 UE-V 에이전트 업그레이드를 자동화 하 고 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="e4d7d-307">**권장 사항:** 컴퓨팅 환경에서 모든 UE-V 1.0 에이전트를 업그레이드 하는 것이 좋지만, 꼭 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="e4d7d-308">UE-V 2. x 설정 위치 템플릿은 설정 저장소 경로의 설정만 공유 하므로 UE-V 1.0 에이전트와 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="e4d7d-309">그러나 관리를 간소화 하 고 UE-V를 지원 하기 위해 배포를 단일 에이전트 버전으로 이동 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="e4d7d-310">업그레이드 실패 후 UE-V 에이전트 복구</span><span class="sxs-lookup"><span data-stu-id="e4d7d-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="e4d7d-311">다음 작업 중 하나를 시도한 후 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="e4d7d-312">UE-V 1.0에서 UE-V 2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="e4d7d-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="e4d7d-313">예를 들어 Windows 7에서 Windows 8으로 또는 Windows 8에서 Windows 8.1까지 최신 버전의 Windows로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="e4d7d-314">UE-V Agent를 업그레이드 한 후 에이전트 제거</span><span class="sxs-lookup"><span data-stu-id="e4d7d-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="e4d7d-315">문제를 해결 하려면 에이전트가 설치 된 컴퓨터의 명령 프롬프트에이 명령을 입력 하 여 UE-V 에이전트 복구를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="e4d7d-316">그런 다음 최신 버전의 UE-V Agent를 설치 하 여 제거 프로세스나 업그레이드를 다시 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4d7d-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="e4d7d-317">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e4d7d-317">Related topics</span></span>


[<span data-ttu-id="e4d7d-318">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="e4d7d-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="e4d7d-319">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포</span><span class="sxs-lookup"><span data-stu-id="e4d7d-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









