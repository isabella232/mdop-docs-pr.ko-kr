---
title: Application Virtualization Client 문제 해결 정보
description: Application Virtualization Client 문제 해결 정보
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815193"
---
# <span data-ttu-id="0fb7e-103">Application Virtualization Client 문제 해결 정보</span><span class="sxs-lookup"><span data-stu-id="0fb7e-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="0fb7e-104">이 항목에서는 Application Virtualization (App-v) 클라이언트의 다양 한 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="0fb7e-105">게시 새로 고침이 매우 느리게 됨</span><span class="sxs-lookup"><span data-stu-id="0fb7e-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="0fb7e-106">특정 컴퓨터의 게시 새로 고침이 예상 보다 오래 걸리므로 클라이언트가 **IconSourceRoot** 설정을 사용 하도록 구성 된 경우 **IconSourceRoot** 에 올바르지 않은 URL이 포함 되어 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="0fb7e-107">유효 하지 않은 URL이 있으면 게시 새로 고침 중 매우 오래 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="0fb7e-108">사용자가 서버에 연결 하 여 연결이 끊긴 작업 모드로 전환할 수 없음</span><span class="sxs-lookup"><span data-stu-id="0fb7e-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="0fb7e-109">RTSPS 프로토콜을 사용 하 여 구성 된 App-v 관리 서버를 사용 하는 경우 사용자가 연결할 수 없고 연결이 끊긴 작업 모드로 전환 되는 경우 서버에서 사용 중인 인증서가 유효한 지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="0fb7e-110">유효 하지 않은 인증서는 사용자가 연결 하는 것을 방지 하 고 연결이 끊긴 작동 모드로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="0fb7e-111">사용자가 응용 프로그램이 완전히 캐시 되지 않은 경우 성능이 느려지는 문제가 발생 함</span><span class="sxs-lookup"><span data-stu-id="0fb7e-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="0fb7e-112">응용 프로그램이 완전히 캐시 되지 않은 경우에는 사용자가 응용 프로그램을 시작 하거나 사용할 때 일시적인 성능이 간헐적으로 느려지는 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="0fb7e-113">이 문제가 발생할 수 있는 몇 가지 이유는 다음과 같습니다 (예: App-v 클라이언트가 응용 프로그램을 자동으로 로드 하는 과정 또는 순서 대로 요청이 처리 되는 경우).</span><span class="sxs-lookup"><span data-stu-id="0fb7e-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="0fb7e-114">응용 프로그램이 완전히 캐시 되 면 이러한 문제가 더 이상 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="0fb7e-115">업데이트가 제거 된 후 표시 되는 오류</span><span class="sxs-lookup"><span data-stu-id="0fb7e-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="0fb7e-116">다음과 같이 올바른 Windows Installer 3.1 명령 형식을 사용 하 여 앱-V 클라이언트에서 업데이트를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="0fb7e-117">이전 명령 형식을 사용 하면 `msiexec /package <GUID> /uninstall <GUID>` 오류 6003 "Application 가상화 클라이언트를 시작할 수 없습니다."가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="0fb7e-118">응용 프로그램을 시작 하려고 할 때 발생 하는 오류 코드 0A-0000E01E</span><span class="sxs-lookup"><span data-stu-id="0fb7e-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="0fb7e-119">오류 코드 0A-0000E01E는 시퀀싱 된 응용 프로그램 패키지가 손상 되었을 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="0fb7e-120">해결 방법은 패키지를 resequence 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="0fb7e-121">사용자가 Q: 드라이브에서 만든 파일에 액세스할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="0fb7e-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="0fb7e-122">사용자가 **Q:** 드라이브에 파일을 저장 하는 경우 드라이브에 대 한 읽기 권한이 없기 때문에 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="0fb7e-123">사용자는 파일을 **Q:** 드라이브에 저장 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="0fb7e-124">사용자에 게 1D1 오류가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="0fb7e-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="0fb7e-125">파일 스트리밍 URL이 OSD (Open Software Descriptor) 파일에서 잘못 설정 된 경우 App-v 클라이언트는 "파일을 찾을 수 없습니다." 오류가 발생 하는 대신 1d1 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="0fb7e-126">이 오류는 응용 프로그램 시작이 실패 하 고 사용자가 강제로 연결이 끊긴 작업 모드로 전환 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="0fb7e-127">파일 스트리밍 URL을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="0fb7e-128">일부 응용 프로그램과 관련 된 잘못 된 아이콘</span><span class="sxs-lookup"><span data-stu-id="0fb7e-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="0fb7e-129">게시 작업에 아이콘을 사용 하는 경우 App-v 클라이언트는 먼저 게시 작업에 지정 된 아이콘의 경로와 원래 원본 경로가 일치 하는 항목에 대 한 아이콘 캐시를 검색 하 여 아이콘의 캐시 된 복사본을가지고 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="0fb7e-130">앱-V 클라이언트가 일치 하는 항목을 찾으면 이미 캐시 된 아이콘을 사용 하 게 됩니다. 그렇지 않으면 새 아이콘이 캐시로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="0fb7e-131">아이콘 경로가 스크래치 디렉터리 이거나 새 아이콘 또는 패키지에 다시 사용 되는 경우 캐시의 조회가 이전 작업에서 잘못 된 아이콘을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="0fb7e-132">사용자가 응용 프로그램을 시작할 때 자격 증명을 묻는 메시지가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="0fb7e-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="0fb7e-133">사용자가 시스템 관리자가 액세스를 제한 한 가상 응용 프로그램을 시작 하려고 하면 사용자에 게 자격 증명을 입력 하 라는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="0fb7e-134">사용자는 응용 프로그램을 실행할 권한이 있는 계정의 사용자 이름 및 암호를 입력 한 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="0fb7e-135">앱-V 클라이언트를 버전 4.5으로 업그레이드 한 후 게시 새로 고침이 실패 함</span><span class="sxs-lookup"><span data-stu-id="0fb7e-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="0fb7e-136">사용자 데이터 디렉터리가 이전에 비표준 위치에 배치 된 경우 (%*allpeople 프로필*%\\Document\ \Softgrid Client\\Users\\%*username*), 컴퓨터에 대 한 관리자 권한이 없는 사용자는 app-v 클라이언트를 업그레이드 한 후 게시 새로 고침이 실패 하는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="0fb7e-137">업그레이드 중에는 앱-V 클라이언트 전역 데이터 디렉터리 및 모든 하위 디렉터리가 관리자만 사용할 수 있는 제한 된 액세스 권한으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="0fb7e-138">전역 데이터 디렉터리의 하위 디렉터리가 아닌 사용자 데이터 디렉터리를 업그레이드 하기 전에 변경 하 여이 문제를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="0fb7e-139">설치 실패 후 다시 부팅 필요</span><span class="sxs-lookup"><span data-stu-id="0fb7e-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="0fb7e-140">어떤 이유로 든 클라이언트 설치에 실패 하 고 클라이언트를 설치 하려는 후속 시도도 실패 하면 Windows Installer 로그를 확인 하 여 "sftplay 실패, 오류 = 1072" 라는 오류 메시지가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="0fb7e-141">그렇다면 클라이언트를 다시 설치 하기 전에 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="0fb7e-142">손상 된 가상 응용 프로그램 복구</span><span class="sxs-lookup"><span data-stu-id="0fb7e-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="0fb7e-143">어떤 이유로 든 지 Windows Installer 패키지 (MSI) 파일을 사용 하 여 설치 된 가상 응용 프로그램 패키지가 손상 되는 경우 패키지를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="0fb7e-144">Windows Installer에서 사용할 수 있는 복구 기능은 사용자 볼륨을 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="0fb7e-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0fb7e-145">Related topics</span></span>


[<span data-ttu-id="0fb7e-146">Application Virtualization Client 참조</span><span class="sxs-lookup"><span data-stu-id="0fb7e-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





