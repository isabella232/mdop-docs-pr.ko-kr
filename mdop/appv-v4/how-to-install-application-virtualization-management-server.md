---
title: Application Virtualization Management Server 설치 방법
description: Application Virtualization Management Server 설치 방법
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817363"
---
# <span data-ttu-id="dc34f-103">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="dc34f-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="dc34f-104">응용 프로그램 가상화 관리 서버가 클라이언트에 응용 프로그램을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="dc34f-105">대규모 배포에 일반적으로 사용할 수 있는 부하 분산 환경에서는 서버 그룹의 모든 서버가 동일한 응용 프로그램을 스트림 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="dc34f-106">응용 프로그램 가상화 관리 서버에서 다른 응용 프로그램을 게시 하려면 서버를 다른 서버 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="dc34f-107">이 경우에도 서버 그룹의 용량을 늘려야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="dc34f-108">네트워크에서 대상 컴퓨터를 지정한 경우 로그인 계정에 로컬 관리자 권한이 있는 경우 다음 절차를 사용 하 여 응용 프로그램 가상화 관리 서버를 설치 하 고 해당 서버 그룹에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="dc34f-109">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-109">Note</span></span>**  
<span data-ttu-id="dc34f-110">서버 그룹 레코드가 없는 경우 설치 마법사에서이 그룹에 대 한 응용 프로그램 가상화 관리 서버의 구성원 자격 기록도 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="dc34f-111">설치 과정을 완료 한 후 서버를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="dc34f-112">응용 프로그램 가상화 관리 서버를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="dc34f-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="dc34f-113">대상 컴퓨터에 설치 된 응용 프로그램 가상화 관리 서버의 이전 버전을 확인 하 고 필요한 경우 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="dc34f-114">**Microsoft Application Virtualization Management Server 설치** 마법사를 열려면 네트워크에서 **setup.exe** 프로그램 가상화 시스템의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe** 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="dc34f-115">**시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="dc34f-116">사용권 **계약** 페이지에서 사용권 계약을 읽고 사용권 계약에 동의 하는 경우 **동의**함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="dc34f-117">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-117">Click **Next**.</span></span>

5.  <span data-ttu-id="dc34f-118">**정보 등록** 페이지에서 사용자 이름 및 **조직을**입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="dc34f-119">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-119">Click **Next**.</span></span>

6.  <span data-ttu-id="dc34f-120">**설치 유형** 페이지에서 **사용자 지정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="dc34f-121">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-121">Click **Next**.</span></span> <span data-ttu-id="dc34f-122">**사용자 지정 설정** 페이지에서 **응용 프로그램 가상화 서버**를 제외한 모든 application virtualization 시스템 구성 요소를 선택 취소 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="dc34f-123">주의</span><span class="sxs-lookup"><span data-stu-id="dc34f-123">Caution</span></span>**  
    <span data-ttu-id="dc34f-124">컴퓨터에 이미 설치 되어 있는 구성 요소를 **사용자 지정 설정** 창에서 선택 취소 하면 해당 구성 요소가 자동으로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="dc34f-125">**구성 데이터베이스** 페이지의 사용 가능한 서버 목록에서 데이터베이스 서버를 선택 하거나 **다음 호스트 이름 사용** 을 선택 하 고 **서버 이름** 및 **포트 번호** 데이터를 지정 하 여 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="dc34f-126">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-126">Click **Next**.</span></span>

    **<span data-ttu-id="dc34f-127">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-127">Note</span></span>**  
    <span data-ttu-id="dc34f-128">Application Virtualization 관리 서버는 대/소문자 구분 SQL을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="dc34f-129">**연결 보안 모드** 페이지의 드롭다운 목록에서 원하는 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="dc34f-130">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-130">Click **Next**.</span></span>

   **<span data-ttu-id="dc34f-131">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-131">Note</span></span>**  
   <span data-ttu-id="dc34f-132">**보안 연결 모드** 를 설정 하려면 공개 키 인프라에서 서버에 서버 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="dc34f-133">서버에 서버 인증서가 설치 되어 있지 않으면이 옵션을 사용할 수 없으며 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="dc34f-134">네트워크 서비스 계정에 사용 중인 인증서에 대 한 읽기 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="dc34f-135">**TCP 포트 구성** 페이지에서 기본 포트 (554)를 사용 하려면 **기본 포트 사용 (554)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="dc34f-136">사용자 지정 포트를 지정 하려면 **사용자 지정 포트 사용** 을 선택 하 고 사용 될 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="dc34f-137">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-137">Click **Next**.</span></span>

   **<span data-ttu-id="dc34f-138">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-138">Note</span></span>**  
   <span data-ttu-id="dc34f-139">보안 되지 않은 환경에서 서버를 설치 하는 경우 기본 포트 (554)를 사용 하거나 사용자 지정 포트를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="dc34f-140">**관리자 그룹** 페이지에서 **그룹 이름**으로이 서버를 관리 하도록 승인 된 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="dc34f-141">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-141">Click **Next**.</span></span> <span data-ttu-id="dc34f-142">지정 된 그룹을 확인 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="dc34f-143">**기본 공급자 그룹** 페이지에서 기본 공급자 그룹의 이름을 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="dc34f-144">**콘텐츠 경로** 페이지에서 SFT 파일이 저장 되는 대상 컴퓨터의 위치를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="dc34f-145">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-145">Note</span></span>**  
   <span data-ttu-id="dc34f-146">관리 서버의 HTTP 또는 RTSP 포트가 이미 할당 된 경우 새 포트를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="dc34f-147">원하는 포트를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="dc34f-148">**프로그램 설치 준비** 페이지에서 응용 프로그램 가상화 관리 서버를 설치 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="dc34f-149">참고</span><span class="sxs-lookup"><span data-stu-id="dc34f-149">Note</span></span>**  
   <span data-ttu-id="dc34f-150">이 단계를 완료 하려고 할 때 오류 25120이 표시 되는 경우 IIS **관리 스크립트와 도구**를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="dc34f-151">이 Windows 기능을 사용 하도록 설정 하려면 제어판의 **프로그램 및 기능** 을 열고 **Windows 기능 설정/해제**를 선택 하 고 **인터넷 정보 서비스를 탐색 합니다.**</span><span class="sxs-lookup"><span data-stu-id="dc34f-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="dc34f-152">**웹 관리 도구**에서 **IIS 관리 스크립트와 도구**를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="dc34f-153">**설치 마법사를 완료** 한 화면에서 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="dc34f-154">중요</span><span class="sxs-lookup"><span data-stu-id="dc34f-154">Important</span></span>**  
   <span data-ttu-id="dc34f-155">설치를 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="dc34f-156">상태 메시지가 Windows 바탕 화면 알림 영역 위에 깜박입니다. 설치에 성공 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="dc34f-157">메시지가 표시 되 면 컴퓨터를 재부팅할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="dc34f-158">그러나 시스템 성능을 최적화 하기 위해 다시 부팅 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dc34f-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="dc34f-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dc34f-159">Related topics</span></span>


[<span data-ttu-id="dc34f-160">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="dc34f-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









