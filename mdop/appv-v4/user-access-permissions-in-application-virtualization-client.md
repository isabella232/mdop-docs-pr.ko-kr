---
title: Application Virtualization Client의 사용자 액세스 권한
description: Application Virtualization Client의 사용자 액세스 권한
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815118"
---
# <span data-ttu-id="1ef70-103">Application Virtualization Client의 사용자 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="1ef70-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="1ef70-104">응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용 프로그램 가상화** 노드를 마우스 오른쪽 단추로 클릭 하 여 액세스할 수 있는 **속성** 대화 상자에 있는 **사용 권한** 탭에서 관리자는 다양 한 클라이언트 함수를 사용 하는 데 필요한 권한을 사용자에 게 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="1ef70-105">**참고**  사용자 권한을 변경 하기 전에 모든 사용 권한 변경이 조직의 사용자 권한 부여에 대 한 지침과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="1ef70-106">다음 표에서는 사용자에 게 부여할 수 있는 사용 권한을 나열 하 고 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ef70-107">사용 권한 이름</span><span class="sxs-lookup"><span data-stu-id="1ef70-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="1ef70-108">설명</span><span class="sxs-lookup"><span data-stu-id="1ef70-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-109">응용 프로그램 추가</span><span class="sxs-lookup"><span data-stu-id="1ef70-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-110">sfttray.exe, sftmime.exe 또는 MMC를 사용 하 여 새 OSD 파일을 클라이언트에 전달 하 여 새 응용 프로그램을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-111">파일 시스템 캐시 크기 변경</span><span class="sxs-lookup"><span data-stu-id="1ef70-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-112">파일 시스템 캐시의 크기를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-113">파일 시스템 드라이브 변경</span><span class="sxs-lookup"><span data-stu-id="1ef70-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-114">파일 시스템에 대해 다른 기본 설정 드라이브 문자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-115">로그 설정 변경</span><span class="sxs-lookup"><span data-stu-id="1ef70-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-116">클라이언트 로그 파일의 로그 수준 또는 로그 경로를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-117">OSD 파일 변경</span><span class="sxs-lookup"><span data-stu-id="1ef70-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-118">등록 된 응용 프로그램의 OSD 파일을 수정 하 여 클라이언트에 게 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="1ef70-119">이는 게시 새로 고침에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-120">응용 프로그램 설정 지우기</span><span class="sxs-lookup"><span data-stu-id="1ef70-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-121">현재 사용자의 파일 형식, 바로 가기 및 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-122">응용 프로그램 삭제</span><span class="sxs-lookup"><span data-stu-id="1ef70-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-123">컴퓨터의 모든 사용자에 대 한 파일 시스템 및 OSD 캐시에서 응용 프로그램에 대 한 참조를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-124">응용 프로그램을 캐시로 가져오기</span><span class="sxs-lookup"><span data-stu-id="1ef70-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-125">지정 된 SFT 파일에서 파일 시스템 캐시로 직접 응용 프로그램 데이터를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="1ef70-126">이는 모든 사용자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-127">캐시에 응용 프로그램 로드</span><span class="sxs-lookup"><span data-stu-id="1ef70-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-128">앱-V 스트리밍 서버와 같이 구성 된 원본에서 응용 프로그램의 SFT 파일 로드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="1ef70-129">이렇게 하면 컴퓨터의 모든 사용자에 대해 응용 프로그램이 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-130">캐시에서 응용 프로그램 잠금 및 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="1ef70-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-131">파일 시스템 캐시에서 응용 프로그램을 언로드하는 것을 금지 하거나 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="1ef70-132">이는 컴퓨터의 모든 사용자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-133">파일 형식 연결 관리</span><span class="sxs-lookup"><span data-stu-id="1ef70-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-134">현재 사용자의 파일 형식 연결만 추가, 수정 또는 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-135">게시 새로 고침 설정 관리</span><span class="sxs-lookup"><span data-stu-id="1ef70-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-136">컴퓨터의 모든 사용자에 대 한 게시 새로 고침 타이밍을 제어 하는 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-137">게시 서버 관리</span><span class="sxs-lookup"><span data-stu-id="1ef70-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-138">컴퓨터의 모든 사용자에 대 한 게시 서버를 추가, 수정 또는 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="1ef70-139">이 권한에는 암시적으로 게시 새로 고침 설정을 관리할 수 있는 사용 권한이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-140">바로 가기 게시</span><span class="sxs-lookup"><span data-stu-id="1ef70-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-141">등록 된 응용 프로그램에 대 한 바로 가기를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="1ef70-142">또한 사용자는 로컬 파일 시스템에서 파일을 만들 수 있는 권한도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-143">응용 프로그램 복구</span><span class="sxs-lookup"><span data-stu-id="1ef70-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-144">바로 가기 또는 파일 형식 연결을 제거 하지 않고 현재 사용자의 응용 프로그램 관련 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-145">게시 새로 고침 시작</span><span class="sxs-lookup"><span data-stu-id="1ef70-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-146">현재 사용자에 대해 예약 되지 않은 게시 새로 고침을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-147">오프 라인 모드 전환</span><span class="sxs-lookup"><span data-stu-id="1ef70-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-148">모든 사용자의 온라인에서 오프 라인 모드로 전체 클라이언트를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ef70-149">캐시에서 응용 프로그램 언로드</span><span class="sxs-lookup"><span data-stu-id="1ef70-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-150">사용자 관련 설정, 바로 가기 또는 파일 형식 연결을 제거 하지 않고 모든 사용자의 파일 시스템 캐시에서 응용 프로그램 데이터를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ef70-151">모든 응용 프로그램 보기</span><span class="sxs-lookup"><span data-stu-id="1ef70-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ef70-152">사용자가 컴퓨터에 등록 된 모든 사용자에 대 한 가상 응용 프로그램을 볼 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef70-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ef70-153">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1ef70-153">Related topics</span></span>


[<span data-ttu-id="1ef70-154">사용자 액세스 권한을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="1ef70-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





