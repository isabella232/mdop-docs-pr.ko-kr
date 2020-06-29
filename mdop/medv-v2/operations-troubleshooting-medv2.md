---
title: 작업 문제 해결
description: 작업 문제 해결
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812740"
---
# <span data-ttu-id="deb8b-103">작업 문제 해결</span><span class="sxs-lookup"><span data-stu-id="deb8b-103">Operations Troubleshooting</span></span>


<span data-ttu-id="deb8b-104">이 항목에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에서 일반적인 운영 문제를 해결 하는 데 사용할 수 있는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="deb8b-105">MED-V 작업의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="deb8b-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="deb8b-106">다음은 이러한 문제를 해결 하는 데 도움이 되도록 MED-V와 솔루션을 실행할 때 발생할 수 있는 최종 사용자의 몇 가지 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="deb8b-107">**문서 리디렉션이 실패**합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="deb8b-108">일반적으로이 문제는 최종 사용자의 내 문서 폴더가 네트워크 위치를 가리키는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="deb8b-109">Windows는 다른 공유 폴더에서 공유를 만드는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="deb8b-110">드라이브나 폴더가 게스트로 리디렉션되는 경우 RDP\\Windows 가상 PC에서 해당 폴더에 대 한 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="deb8b-111">따라서 호스트의 내 문서 폴더가 이미 공유를 가리키고 있는 경우 RDP\\Windows Virtual PC에서 공유 공유를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="deb8b-112">이 문제의 또 다른 가능한 원인은 네트워크 리소스에 연결 하는 데 필요한 자격 증명이 사용자의 도메인 자격 증명과 다를 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="deb8b-113">MED-V는 호스트가 호스트에서 리디렉션되는 것을 감지 하 여 해당 정보를 게스트로 보낸 다음 네트워크 리소스를 다시 연결 하려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="deb8b-114">사용자의 자격 증명이 인증 되지 않으면 MED-V가 인증 시도를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="deb8b-115">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-115">Solution</span></span>**

<span data-ttu-id="deb8b-116">이 문제를 해결 하려면 다음 중 하나를 시도해 보세요.</span><span class="sxs-lookup"><span data-stu-id="deb8b-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="deb8b-117">Active Directory 내에서 사용자의 루트 디렉터리를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="deb8b-118">그런 다음 게스트와 호스트가 동일한 네트워크 리소스에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="deb8b-119">내 문서 폴더를 UNC 경로로 리디렉션하는 대신 호스트의 드라이브 문자에 매핑하여 네트워크 리소스를 가리키는 드라이브를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="deb8b-120">그런 다음 내 문서 폴더를 UNC 경로 대신 드라이브 문자를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="deb8b-121">그런 다음 게스트는 예상 대로 동일한 매핑된 드라이브로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="deb8b-122">게스트에서 내 문서 폴더를 네트워크 리소스로 리디렉션하고 필요에 따라 추가 자격 증명을 제공 하는 시작 스크립트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="deb8b-123">**URL 전환에 실패**했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="deb8b-124">호스트에서 게스트로 리디렉션 하도록 지정한 URL이 의도 한 대로 리디렉션되어 있지 않거나 웹 사이트가 없다는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="deb8b-125">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-125">Solution</span></span>**

<span data-ttu-id="deb8b-126">이 오류는 URL 리디렉션 정보에 별표 (\ \*) 등의 문자를 잘못 사용 하거나 철자가 틀린 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="deb8b-127">레지스트리 값이 URL 리디렉션 인지 확인 하 고 오류를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="deb8b-128">레지스트리 키는 `RedirectUrls` 다음과 같이 호출 되며 일반적으로 다음 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="deb8b-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="deb8b-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="deb8b-130">**작업 표시줄의 잘못**되는 아이콘</span><span class="sxs-lookup"><span data-stu-id="deb8b-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="deb8b-131">기본적으로 최종 사용자의 게시 된 응용 프로그램 및 리디렉션된 Url에 대 한 작업 표시줄에 표시 되는 아이콘은 Windows 가상 PC의 아이콘입니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="deb8b-132">최종 사용자가이 기본 동작을 인식 하지 못하는 경우 작업 표시줄을 보면서 해당 응용 프로그램을 찾을 때 혼동 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="deb8b-133">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-133">Solution</span></span>**

<span data-ttu-id="deb8b-134">이 기본 동작을 방지 하는 유일한 방법은 다음과 같이 작업 표시줄 속성에 대 한 사용자 설정을 변경 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="deb8b-135">작업 표시줄을 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="deb8b-136">**작업 표시줄 및 시작 메뉴 속성** 대화 상자에서 **작업 표시줄** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="deb8b-137">**작업 표시줄 단추** 상자의 드롭다운 표시줄에서 **결합 안 함을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="deb8b-138">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-138">Click **OK**.</span></span>

<span data-ttu-id="deb8b-139">게시 된 응용 프로그램 및 리디렉션된 Url에 대해 필요한 아이콘이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="deb8b-140">**두 번째 사용자가 로그온을 시도 하거나 가상 컴퓨터를 사용 중인 경우 경고가 발행**됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="deb8b-141">첫 번째 사용자가 MED-V를 계속 실행 하는 동안 두 번째 사용자가 MED-V 작업 영역에 로그온 할 때 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="deb8b-142">가상 컴퓨터를 사용 하는 동안 (예: **시작** 메뉴의 WINDOWS 가상 PC를 통해 가상 컴퓨터를 시작 하는 경우)이 경고가 발생 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="deb8b-143">최종 사용자가 경고 메시지를 수락 하면 MED-V가 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="deb8b-144">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-144">Solution</span></span>**

<span data-ttu-id="deb8b-145">최종 사용자가 로그온 하기 전에 다른 모든 사용자가 MED-V에 로그 오프 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="deb8b-146">이렇게 하면 MED-V의 다른 인스턴스가 실행 되 고 있지 않고 Windows 가상 PC가 가상 컴퓨터의 제어권을 받지 않게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="deb8b-147">**처음 설정 하는 동안 경고음이 들립니다**.</span><span class="sxs-lookup"><span data-stu-id="deb8b-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="deb8b-148">경우에 따라 MED-V가 처음 설치를 실행 하는 동안 경고음이 들립니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="deb8b-149">이는 최종 사용자에 게 혼란 스 러 울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-149">This can be confusing to an end user.</span></span> <span data-ttu-id="deb8b-150">비프음은 종료와 같은 특정 작업을 수행할 때 가상 머신에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="deb8b-151">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-151">Solution</span></span>**

<span data-ttu-id="deb8b-152">각 가상 컴퓨터 시작 순서의 시작 부분에 "net stop beep" 명령을 지정 하 여 신호음 서비스를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="deb8b-153">또는 "sc config beep 시작 = disabled" 명령을 지정 하 여 신호음 서비스를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="deb8b-154">이미지를 봉인 하거나 Sysprep의 일부로 이러한 명령을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="deb8b-155">연결 **모드의 Med-v 작업 영역에 대해 생성 된 여러 네트워크 연결**</span><span class="sxs-lookup"><span data-stu-id="deb8b-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="deb8b-156">처음 설치 프로그램이 NAT 모드에 맞게 구성 된 MED-V 작업 영역을 만드는 경우 Windows 가상 PC에 단일 네트워크 연결만 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="deb8b-157">그러나 처음 설치 프로그램이 브리지 모드에 대해 구성 된 MED-V 작업 영역을 만드는 경우 MED-V가 활성 상태인 네트워크 어댑터를 확인할 수 없기 때문에 컴퓨터에 설치 된 각 네트워크 어댑터에 대해 별도의 네트워크 연결이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="deb8b-158">이는 또한 로밍 사용자가 항상 유선 및 무선 연결에 사용할 수 있는 네트워크 어댑터를 보유 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="deb8b-159">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-159">Solution</span></span>**

<span data-ttu-id="deb8b-160">없음.</span><span class="sxs-lookup"><span data-stu-id="deb8b-160">None.</span></span>

<span data-ttu-id="deb8b-161">**Med-v 응용 프로그램이 닫히는 동안 너무 오랫동안 응답 하지 않습니다**.</span><span class="sxs-lookup"><span data-stu-id="deb8b-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="deb8b-162">어떤 경우에는 MED-V 응용 프로그램이 닫으려고 할 때 응답을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="deb8b-163">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-163">Solution</span></span>**

<span data-ttu-id="deb8b-164">게스트 가상 컴퓨터에서 WaitToKillAppTimeout 레지스트리 키를 설정 하 여 응답 하지 않는 응용 프로그램을 닫기 위해 MED-V가 대기 하는 시간을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="deb8b-165">자세한 내용은 [WINDOWS XP에서 프로세스가 올바르게 종료 될 수 있도록 시스템 종료 시간을 늘리는 방법을](https://go.microsoft.com/fwlink/?LinkId=206819) 참조 하세요 ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="deb8b-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="deb8b-166">**게스트 가상 머신에서 게시 된 응용 프로그램 바로 가기의 이름을 바꾸면 호스트에서 게시 된 이름이 변경 되지**않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="deb8b-167">바로 가기를 만든 다음 게스트 가상 컴퓨터에서 바로 가기의 이름을 변경 하 여 응용 프로그램을 게시 하면 원래 응용 프로그램 이름이 호스트 **시작** 메뉴에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="deb8b-168">프로그램이 예상 대로 계속 실행 되지만, 프로그램에는 항상 원래 이름이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="deb8b-169">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-169">Solution</span></span>**

<span data-ttu-id="deb8b-170">없음.</span><span class="sxs-lookup"><span data-stu-id="deb8b-170">None.</span></span> <span data-ttu-id="deb8b-171">이는 Windows 가상 PC의 알려진 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="deb8b-172">**게스트 가상 머신에서 바로 가기를 이동 해도 호스트 컴퓨터 시작 메뉴의 위치는 업데이트 되지**않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="deb8b-173">호스트 컴퓨터 **시작** 메뉴에 게시 되는 med-v 응용 프로그램 바로 가기는 레지스트리에 카탈로그로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="deb8b-174">응용 프로그램 바로 가기를 하위 폴더로 이동 하면 레지스트리가 업데이트 되어 변경 내용이 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="deb8b-175">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-175">Solution</span></span>**

<span data-ttu-id="deb8b-176">MED-V 응용 프로그램 바로 가기의 위치를 변경 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="deb8b-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="deb8b-177">MED-V가 실행 되는 경우 MED-V 게스트 가상 컴퓨터에서 Windows 탐색기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="deb8b-178">"%Allpeople Profile%\\start Menu\\Programs" 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="deb8b-179">Startmenu 또는 프로그램 폴더 밖으로 응용 프로그램 바로 가기를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="deb8b-180">약 30 초가 지난 후 호스트 컴퓨터의 **시작** 메뉴에서 바로 가기가 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="deb8b-181">응용 프로그램 바로 가기를 시작 단추 \ 프로그램 디렉터리 아래의 새 프로그램 폴더로 다시 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="deb8b-182">약 30 초가 지난 후 호스트 컴퓨터의 **시작** 메뉴에서 바로 가기가 업데이트 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="deb8b-183">**게시 된 응용 프로그램은 유휴 상태가 되 고 나 서 시간이 초과 될 수 있습니다**.</span><span class="sxs-lookup"><span data-stu-id="deb8b-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="deb8b-184">일부 경우에는 게시 된 응용 프로그램에 잠시 동안 유휴 상태에 있는 경우 시간이 초과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="deb8b-185">이 상황은 IPsec을 사용할 수 있고, MED-V 작업 영역이 NAT 모드에 대해 구성 된 경우에만 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="deb8b-186">브리지 모드로 실행 하는 경우에는 이러한 상황이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="deb8b-187">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-187">Solution</span></span>**

<span data-ttu-id="deb8b-188">NAT 모드에서 MED-V 작업 영역을 실행 중인 경우 IPsec을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="deb8b-189">**게시 된 응용 프로그램을 작업 표시줄에 고정 하면 med-v가 무시**됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="deb8b-190">최종 사용자가 게시 된 응용 프로그램을 작업 표시줄에 고정 한 다음 응용 프로그램을 닫으면 다음 번에 작업 표시줄 아이콘에서 응용 프로그램을 열 때 MED-V가 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="deb8b-191">대신 응용 프로그램이 VMSAL 창에서 바로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="deb8b-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="deb8b-192">해결 방법</span><span class="sxs-lookup"><span data-stu-id="deb8b-192">Solution</span></span>**

<span data-ttu-id="deb8b-193">MED-V에 게시 된 응용 프로그램을 작업 표시줄에 고정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="deb8b-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="deb8b-194">관련 항목</span><span class="sxs-lookup"><span data-stu-id="deb8b-194">Related topics</span></span>


[<span data-ttu-id="deb8b-195">MED-V 작업의 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="deb8b-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="deb8b-196">배포 문제 해결</span><span class="sxs-lookup"><span data-stu-id="deb8b-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





