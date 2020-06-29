---
title: App-V로 폴더 리디렉션 사용 계획
description: App-V로 폴더 리디렉션 사용 계획
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813385"
---
# <span data-ttu-id="0b672-103">App-V로 폴더 리디렉션 사용 계획</span><span class="sxs-lookup"><span data-stu-id="0b672-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="0b672-104">Microsoft App-v (Application Virtualization) 5.1는 사용자 및 관리자가 폴더 경로를 새 위치로 리디렉션할 수 있는 기능인 폴더 리디렉션 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-104">Microsoft Application Virtualization (App-V) 5.1 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="0b672-105">이 항목의 섹션:</span><span class="sxs-lookup"><span data-stu-id="0b672-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0b672-106">폴더 리디렉션 사용에 대 한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0b672-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="0b672-107">앱과 함께 사용 하도록 폴더 리디렉션을 구성 하는 방법-V</span><span class="sxs-lookup"><span data-stu-id="0b672-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="0b672-108">App-V에서 폴더 리디렉션이 작동 하는 방식</span><span class="sxs-lookup"><span data-stu-id="0b672-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="0b672-109">폴더 리디렉션 개요</span><span class="sxs-lookup"><span data-stu-id="0b672-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="0b672-110">폴더 리디렉션 사용을 위한 요구 사항 및 지원 되지 않는 시나리오</span><span class="sxs-lookup"><span data-stu-id="0b672-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b672-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="0b672-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-112">% AppData% 폴더 리디렉션을 사용 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b672-113">AppData 가상 파일 시스템 (VFS) 폴더가 있는 App-v 패키지를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="0b672-114">폴더 리디렉션을 사용 하도록 설정 하 고 사용자의 폴더를 공유 폴더 (일반적으로 네트워크 폴더)로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="0b672-115">다음 두 가지 모두 또는 모두 로밍:</span><span class="sxs-lookup"><span data-stu-id="0b672-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b672-116">%Appdata%\Microsoft\AppV\Client\Catalog 아래에 있는 파일</span><span class="sxs-lookup"><span data-stu-id="0b672-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="0b672-117">HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages의 레지스트리 설정</span><span class="sxs-lookup"><span data-stu-id="0b672-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="0b672-118">자세한 내용은 <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> 응용 프로그램 게시 및 클라이언트 조작을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="0b672-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="0b672-119">App-v 5.0 SP2 이상 클라이언트를 실행 하는 컴퓨터에 로그인 하는 각 사용자가 다음 폴더를 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b672-120">% AppData%가 원하는 네트워크 위치로 구성 되어 <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> 있습니다 (오프 라인 파일 지원 여부에 관계 없이 </a> ).</span><span class="sxs-lookup"><span data-stu-id="0b672-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="0b672-121">% LocalAppData%가 원하는 로컬 폴더로 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b672-122">지원되지 않는 시나리오</span><span class="sxs-lookup"><span data-stu-id="0b672-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b672-123">% LocalAppData%을 (를) 네트워크 드라이브로 구성 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="0b672-124">여러 사용자를 위해 시작 메뉴를 단일 폴더로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="0b672-125">로밍 AppData (% AppData%) 이 (가) 사용할 수 없는 네트워크 공유로 리디렉션 되었습니다. 앱 V 응용 프로그램은 다음과 같이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b672-126">App-V 버전</span><span class="sxs-lookup"><span data-stu-id="0b672-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="0b672-127">시나리오 설명</span><span class="sxs-lookup"><span data-stu-id="0b672-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b672-128">앱-V 5.0 SP2 plus 핫픽스를 통해 app-v 5.0</span><span class="sxs-lookup"><span data-stu-id="0b672-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-129">이 오류는 오프 라인 파일을 사용할 수 있는지 여부에 관계 없이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b672-130">App-v 5.0 SP3 이상</span><span class="sxs-lookup"><span data-stu-id="0b672-130">In App-V 5.0 SP3 and later</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-131">사용할 수 없는 네트워크 공유가 오프 라인 파일에 대해 사용 하도록 설정 된 경우 App-v 응용 프로그램이 성공적으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="0b672-132">앱과 함께 사용 하도록 폴더 리디렉션을 구성 하는 방법-V</span><span class="sxs-lookup"><span data-stu-id="0b672-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="0b672-133">폴더 리디렉션은 데스크톱, 내 문서, 내 사진 등의 다른 폴더에 적용할 수 있습니다. 그러나 앱 V 응용 프로그램 사용에 영향을 주는 유일한 폴더는 사용자의 로밍 AppData 폴더 (% AppData%)입니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="0b672-134">앱-V에 영향을 주지 않고 폴더 리디렉션을 지원 되는 다른 모든 폴더에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="0b672-135">App-V에서 폴더 리디렉션이 작동 하는 방식</span><span class="sxs-lookup"><span data-stu-id="0b672-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="0b672-136">다음 표에서 는% AppData%가 네트워크로 리디렉션되는 경우와이 문서의 앞 부분에 나열 된 요구 사항을 충족 하는 경우 폴더 리디렉션이 작동 하는 방식을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b672-137">가상 환경 상태</span><span class="sxs-lookup"><span data-stu-id="0b672-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="0b672-138">발생 하는 작업</span><span class="sxs-lookup"><span data-stu-id="0b672-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b672-139">가상 환경이 시작 되는 경우</span><span class="sxs-lookup"><span data-stu-id="0b672-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-140">VFS (가상 파일 시스템) AppData 폴더는 로컬 AppData 폴더 (% LocalAppData%)에 매핑됩니다. 사용자의 로밍 AppData 폴더 (% AppData%)를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="0b672-141">LocalAppData에는 사용 중인 패키지에 대 한 사용자 로밍 AppData 폴더의 로컬 캐시가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="0b672-142">로컬 캐시의 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="0b672-143">사용자의 로밍 AppData 폴더에서 최신 데이터를 복사 하 여 현재 로컬 캐시에 있는 데이터에 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="0b672-144">가상 환경이 실행 되는 동안에는 데이터가 계속 로컬 캐시에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="0b672-145">데이터 는% LocalAppData% 밖에만 제공 되며, 최종 사용자가 컴퓨터를 종료할 때 까지% AppData%로 이동 하거나 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="0b672-146">AppData 폴더에 대 한 항목은 시스템 컨텍스트가 아닌 사용자 컨텍스트를 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="0b672-147">참고</span><span class="sxs-lookup"><span data-stu-id="0b672-147">Note</span></span></strong><br/><p><span data-ttu-id="0b672-148">App-v 클라이언트 폴더 리디렉션은 파일 을% AppData% 에서% LocalAppData%까지 이동 하지 못하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="0b672-149"><a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">앱-V 5.0 SP2에 대 한 릴리스 정보를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="0b672-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b672-150">가상 환경이 종료 되는 경우</span><span class="sxs-lookup"><span data-stu-id="0b672-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-151">AppData (로밍)의 로컬 캐시 된 데이터가 압축 되 고 "실제" 로밍 AppData 폴더 (% AppData%)에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="0b672-152">마지막으로 알려진 업로드가 표시 된 타임 스탬프는 다음의 레지스트리 키로 동시에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="0b672-153">중복성을 제공 하기 위해 App-v는 압축 된 데이터의 가장 최근 복사본 3 개 를% AppData%로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-153">To provide redundancy, App-V keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="0b672-154">폴더 리디렉션 개요</span><span class="sxs-lookup"><span data-stu-id="0b672-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b672-155">목적</span><span class="sxs-lookup"><span data-stu-id="0b672-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-156">로컬 드라이브에 파일이 있는 것 처럼 최종 사용자가 다른 폴더로 리디렉션되는 파일로 작업할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b672-157">설명</span><span class="sxs-lookup"><span data-stu-id="0b672-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-158">폴더 리디렉션을 통해 사용자와 관리자는 폴더의 경로를 네트워크 위치로 리디렉션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="0b672-159">폴더의 문서는 네트워크의 모든 컴퓨터에서 사용자가 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="0b672-160">폴더 리디렉션을 통해 사용자와 관리자는 폴더의 경로를 네트워크 위치로 리디렉션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="0b672-161">폴더의 문서는 네트워크의 모든 컴퓨터에서 사용자가 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="0b672-162">새 위치는 로컬 컴퓨터의 폴더 이거나 공유 네트워크의 폴더 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="0b672-163">폴더 리디렉션은 파일을 즉시 업데이트 하는 반면, 로밍 데이터는 일반적으로 사용자가 로그인 하거나 로그 오프할 때 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b672-164">사용 예제</span><span class="sxs-lookup"><span data-stu-id="0b672-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b672-165">일반적으로 컴퓨터&#39;s 로컬 하드 디스크에 저장 된 문서 폴더를 네트워크 위치에 리디렉션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="0b672-166">사용자는 네트워크의 모든 컴퓨터에서 폴더의 문서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b672-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b672-167">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="0b672-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="0b672-168">폴더 리디렉션 개요</span><span class="sxs-lookup"><span data-stu-id="0b672-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















