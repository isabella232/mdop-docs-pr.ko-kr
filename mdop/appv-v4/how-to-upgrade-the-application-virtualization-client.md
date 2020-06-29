---
title: Application Virtualization Client를 업그레이드하는 방법
description: Application Virtualization Client를 업그레이드하는 방법
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816453"
---
# <span data-ttu-id="8d9a6-103">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="8d9a6-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="8d9a6-104">다음 절차를 사용 하 여 원격 데스크톱 서비스 (이전의 터미널 서비스)의 Application Virtualization (App-v) 데스크톱 클라이언트 또는 App-v 클라이언트를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="8d9a6-105">이전에 설치 된 이전 버전을 통해 새 버전을 설치 하 여 클라이언트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="8d9a6-106">클라이언트를 업그레이드할 때 설치 관리자 소프트웨어는 자동으로 사용자의 가상 응용 프로그램 설정을 유지 하 고 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="8d9a6-107">설치 프로그램을 실행 하려면 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="8d9a6-108">**참고**  Application Virtualization (App-v) 4.5 이상 버전으로 업그레이드 하는 동안 HKCU 레지스트리 키에 대 한 사용 권한이 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="8d9a6-109">이 때문에 사용자가 연결이 끊긴 사용자 구성 모드 설정과 같이 이전에 설정한 사용자 구성은 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="8d9a6-110">사용자가 사용 권한 잠금을 통해 클라이언트 사용자 인터페이스 동작을 실제로 제한 하지 않는 경우 사용자는 게시 새로 고침 후 이러한 기본 설정을 다시 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="8d9a6-111">**중요**  App-v 클라이언트의 버전 4.6 또는 이후 버전으로 업그레이드 하는 경우 컴퓨터의 운영 체제 32 비트 또는 64 비트에 대 한 올바른 설치 관리자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="8d9a6-112">설치에 실패 하 고 잘못 된 설치 관리자를 사용 하는 경우 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="8d9a6-113">Application Virtualization 데스크톱 클라이언트를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="8d9a6-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="8d9a6-114">모든 가상 응용 프로그램을 종료 하 고 Windows 바탕 화면 알림 영역에 표시 되는 App-v 데스크톱 클라이언트 아이콘을 마우스 오른쪽 단추로 클릭 한 다음 **끝내기** 를 선택 하 여 기존 클라이언트를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="8d9a6-115">올바른 설치 관리자 보관 파일을 가져와 컴퓨터에 저장 한 후에 두 번 클릭 하 여 보관을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="8d9a6-116">setup.exe 파일을 찾아 두 번 클릭 하 setup.exe 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="8d9a6-117">마법사는 시스템을 확인 하 여 모든 필수 소프트웨어를 설치 했는지 확인 하 고 누락 된 경우 다음 중 하나를 설치 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="8d9a6-118">Microsoft VisualC + + 2005SP1 재배포 가능 패키지 (x86)</span><span class="sxs-lookup"><span data-stu-id="8d9a6-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="8d9a6-119">MSXML (Microsoft Core XML Services) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="8d9a6-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="8d9a6-120">Microsoft 응용 프로그램 오류 보고</span><span class="sxs-lookup"><span data-stu-id="8d9a6-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="8d9a6-121">**참고**  4.6 이상 버전의 경우 마법사는 다음 소프트웨어 필수 구성 요소도 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="8d9a6-122">Microsoft VisualC + + 2008 SP1 재배포 가능 패키지 (x86)</span><span class="sxs-lookup"><span data-stu-id="8d9a6-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="8d9a6-123">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-123">Click **Install**.</span></span> <span data-ttu-id="8d9a6-124">설치 진행률이 표시 되 고 상태가 **보류 중** 으로 변경 **됩니다.**</span><span class="sxs-lookup"><span data-stu-id="8d9a6-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="8d9a6-125">각 단계가 성공적으로 완료 되 면 설치 상태가 **성공** 으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="8d9a6-126">**응용 프로그램 가상화 데스크톱 클라이언트** 대화 상자가 나타나고 이전 버전의 클라이언트가 컴퓨터에 있음을 알리는 메시지가 표시 되 면 **다음** 을 클릭 하 여 새 버전으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="8d9a6-127">**라이선스 계약** 화면이 표시 되 면 라이선스 계약을 읽고 동의 하는 경우 **사용권 계약에 동의 함을**클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="8d9a6-128">InstallShield 마법사에서 **프로그램을 업그레이드할 준비가 되었습니다** 대화 상자 화면을 표시 하는 경우 **업그레이드** 를 클릭 하 여 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="8d9a6-129">다음 화면은 클라이언트가 설치 되 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="8d9a6-130">**경고가**  1 단계에서 클라이언트 프로그램을 종료 하지 않은 경우 **사용 중인 파일** 경고가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="8d9a6-131">이 문제가 발생 하는 경우 바탕 화면 알림 영역에 표시 된 App-v 클라이언트 아이콘을 마우스 오른쪽 단추로 클릭 하 고 **끝내기** 를 선택 하 여 기존 클라이언트를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="8d9a6-132">그런 다음, **다시 시도** 를 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="8d9a6-133">설치가 성공적으로 완료 되 면 컴퓨터를 다시 시작 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="8d9a6-134">설치를 완료 하려면 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="8d9a6-135">**주의**  사항 어떤 이유로 든 업그레이드가 실패 하는 경우에는 컴퓨터를 다시 시작 해야 업그레이드를 다시 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="8d9a6-136">명령줄을 사용 하 여 Application Virtualization 클라이언트를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="8d9a6-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="8d9a6-137">setup.msi 프로그램을 사용 하 여 App-v 클라이언트를 업그레이드 하는 경우 필수 필수 구성 요소 소프트웨어가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="8d9a6-138">중요</span><span class="sxs-lookup"><span data-stu-id="8d9a6-138">Important</span></span>**  
    -   <span data-ttu-id="8d9a6-139">버전 4.6 이상 App-v 클라이언트의 경우 setup.msi 프로그램이 시스템을 검사 하 고 필수 구성 요소가 설치 되어 있지 않은 경우 설치를 계속할 수 없음을 나타내는 오류 메시지와 함께 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="8d9a6-140">App-v 버전 4.6의 경우 업그레이드 중 명령줄 매개 변수를 사용할 수 없으며 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="8d9a6-141">다음 명령줄 예제에서는 setup.msi 파일을 사용 하 여 App-v 클라이언트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="8d9a6-142">원격 데스크톱 서비스에 대 한 app-v 클라이언트 (이전의 터미널 서비스)를 업그레이드 하 고 있는지 여부에 따라 올바른 클라이언트 설치 프로그램을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="8d9a6-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="8d9a6-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="8d9a6-144">**중요**  값에 공백이 포함 된 경우에만 인용 부호가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="8d9a6-145">일관성을 위해 이전 예제의 모든 인스턴스가 인용 부호로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="8d9a6-146">원격 데스크톱 서비스의 응용 프로그램 가상화 클라이언트를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="8d9a6-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="8d9a6-147">원격 데스크톱 세션 호스트 (RDSession Host) 서버에서 응용 프로그램을 설치 하거나 업그레이드 하기 위해 조직의 표준 정책을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="8d9a6-148">시스템이 팜의 일부인 경우 서버 팜에서 RDSession Host를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="8d9a6-149">원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트를 업그레이드 하려면, RDSession Host에서 수동으로 클라이언트를 업그레이드할 수 없기 때문에 명령줄을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="8d9a6-150">**참고**  App-v 버전 4.6 이상에서는 명령줄을 사용 하 여 클라이언트를 업그레이드 하는 것 외에도 원격 데스크톱 세션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="8d9a6-151">원격 데스크톱 세션을 시작 하는 데 특별 한 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="8d9a6-152">원격 데스크톱 서비스 업그레이드에 대 한 클라이언트가 완료 되 면 다시 시작 하 고 RDSession Host에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="8d9a6-153">시스템을 다시 시작한 후 서버 팜에 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="8d9a6-154">**주의**  사항 어떤 이유로 든 업그레이드가 실패 하는 경우에는 컴퓨터를 다시 시작 해야 업그레이드를 다시 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9a6-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="8d9a6-155">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8d9a6-155">Related topics</span></span>


[<span data-ttu-id="8d9a6-156">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="8d9a6-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





