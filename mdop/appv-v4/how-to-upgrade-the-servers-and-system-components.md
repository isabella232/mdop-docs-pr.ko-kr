---
title: 서버 및 시스템 구성 요소를 업그레이드하는 방법
description: 서버 및 시스템 구성 요소를 업그레이드하는 방법
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816423"
---
# <span data-ttu-id="0e6aa-103">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="0e6aa-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="0e6aa-104">모든 응용 프로그램 가상화 시스템 컴퓨터에 설치 된 소프트웨어 구성 요소를 업그레이드 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="0e6aa-105">응용 프로그램 가상화 시스템 서비스는 업그레이드 된 각 컴퓨터에서 자동으로 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="0e6aa-106">참고</span><span class="sxs-lookup"><span data-stu-id="0e6aa-106">Note</span></span>**  
-   <span data-ttu-id="0e6aa-107">업그레이드 프로세스는 모든 응용 프로그램 가상화 시스템 서비스를 중지 하 여 시스템 서비스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="0e6aa-108">업그레이드 프로세스를 시작 하기 전에 사용자 세션을 종료 해야 하며, 환경에서 모든 Application Virtualization Server 서비스를 중지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="0e6aa-109">응용 프로그램 가상화 데이터베이스에 대 한 액세스를 공유 하는 서버가 두 개 이상인 경우, 데이터베이스를 업그레이드 하는 동안 모든 서버가 오프 라인 상태가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="0e6aa-110">데이터베이스 업그레이드에 대 한 일반적인 비즈니스 관행을 준수 해야 하지만, 테스트 서버에서 먼저 데이터베이스의 백업 복사본을 사용 하 여 데이터베이스 업그레이드를 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="0e6aa-111">그런 다음 데이터베이스 스키마를 업그레이드 하는 첫 번째 업그레이드에 대 한 서버 중 하나를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="0e6aa-112">프로덕션 데이터베이스가 성공적으로 업그레이드 된 후에는 다른 서버를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="0e6aa-113">Microsoft app-v (Application virtualization) 4.5 또는 4.1 SP1으로 업그레이드를 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="0e6aa-114">App-v 4.5로 업그레이드 하기 전에 앱-V 4.0 및 이전 버전을 4.1 또는 4.1 SP1로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="0e6aa-115">응용 프로그램 가상화 시스템 컴퓨터에서 소프트웨어 구성 요소를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="0e6aa-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="0e6aa-116">네트워크에서 설치 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 Setup.exe 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="0e6aa-117">설치 마법사의 **시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="0e6aa-118">**사용권 계약** 페이지에서 사용권 계약을 읽고 **동의**함을 확인 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="0e6aa-119">설치 된 **소프트웨어** 페이지가 열리고 설치 된 응용 프로그램 가상화 시스템 구성 요소 목록과 각 구성 요소의 버전이 표시 되는 경우 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="0e6aa-120">**세션 손실 경고** 페이지에서 표시 된 메시지를 읽은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="0e6aa-121">**구성 데이터베이스에 연결** 페이지에서 페이지의 콘텐츠를 검토 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="0e6aa-122">**데이터베이스 업그레이드 필요** 페이지가 표시 되 면 데이터베이스 업그레이드가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="0e6aa-123">데이터베이스 관리 자격 증명을 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="0e6aa-124">이 페이지가 표시 되지 않으면 9 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="0e6aa-125">**백업 구성 데이터베이스** 페이지에서 해당 상자를 선택 하 여 백업을 수행 하 고 기존 위치로 내보내고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="0e6aa-126">**중요**  업그레이드 실패가 발생 한 경우 이전 버전으로 롤백할 수 있도록 하려면 **구성 데이터베이스의 백업 수행** 확인란을 선택 해야 하며 그렇지 않으면 구성 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="0e6aa-127">VSS를 사용 하 여 데이터베이스를 복원 하려는 경우 먼저 관리 서버에서 App-v 서버 서비스를 중지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="0e6aa-128">같은 데이터베이스에 연결 된 서버가 여러 개 있는 경우 모든 관리 서버에서이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="0e6aa-129">첫 번째 **패키지 유효성 검사** 페이지에서 콘텐츠를 읽은 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="0e6aa-130">두 번째 **패키지 유효성 검사** 페이지에는 패키지 유효성 검사에 대 한 세부 정보를 메모장 창에 표시할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="0e6aa-131">세부 정보를 보려면 **세부 정보**를 클릭 합니다. 그렇지 않으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="0e6aa-132">프로그램을 **업그레이드할 준비가 되었습니다** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="0e6aa-133">**설치 마법사 완료** 페이지에서 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="0e6aa-134">응용 프로그램 가상화 관리 콘솔 또는 응용 프로그램 가상화 서버 소프트웨어 구성 요소를 설치한 다른 모든 컴퓨터에서 1 ~ 12 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="0e6aa-135">데이터 저장소를 업그레이드 한 후 정상 작업을 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e6aa-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="0e6aa-136">(데이터 저장소는 서버 또는 App-v 관리 웹 서비스를 업그레이드할 때 업그레이드 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="0e6aa-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="0e6aa-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0e6aa-137">Related topics</span></span>


[<span data-ttu-id="0e6aa-138">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="0e6aa-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





