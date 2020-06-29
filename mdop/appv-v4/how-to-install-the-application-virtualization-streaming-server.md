---
title: Application Virtualization Streaming Server 설치 방법
description: Application Virtualization Streaming Server 설치 방법
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817328"
---
# <span data-ttu-id="abf04-103">Application Virtualization Streaming Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="abf04-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="abf04-104">Application Virtualization 스트리밍 서버는 응용 프로그램을 클라이언트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="abf04-105">대규모 배포에 일반적으로 사용할 수 있는 부하 분산 환경에서는 서버 그룹의 모든 서버가 동일한 응용 프로그램을 스트림 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="abf04-106">응용 프로그램 가상화 스트리밍 서버가 서로 다른 응용 프로그램을 스트리밍하는 경우 서버를 다른 서버 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="abf04-107">이 경우 서버 그룹의 용량을 늘려야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="abf04-108">네트워크에서 대상 컴퓨터를 지정한 경우 로그온 계정에 로컬 관리자 권한이 있으면 다음 절차를 사용 하 여 Application Virtualization 스트리밍 서버를 설치 하 고 해당 서버 그룹에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="abf04-109">**참고**  설치 마법사가 서버 그룹 레코드 (있는 경우)를 만들 수 있으며,이 그룹에 대 한 응용 프로그램 가상화 스트리밍 서버 구성원의 레코드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="abf04-110">설치 프로세스를 완료 한 후 서버를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="abf04-111">Application Virtualization 스트리밍 서버를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="abf04-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="abf04-112">대상 컴퓨터에 이전 버전의 Application Virtualization 스트리밍 서버가 설치 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="abf04-113">**중요**  이 컴퓨터에 App-v 관리 서버가 설치 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="abf04-114">두 제품을 같은 컴퓨터에 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="abf04-115">네트워크에서 응용 프로그램 가상화 시스템 설정 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe** 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="abf04-116">**시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="abf04-117">**사용권 계약** 페이지에서 사용 조건에 동의 하려면 동의 **함을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="abf04-118">**고객 정보** 페이지에서 **사용자 이름** 및 조직을 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="abf04-119">**설치 경로** 페이지에서 **찾아보기를**클릭 하 고 스트리밍 서버를 설치 하려는 위치를 지정한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="abf04-120">**연결 보안 모드** 페이지의 드롭다운 목록에서 원하는 인증서를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="abf04-121">**참고**  **보안 연결 모드** 를 설정 하려면 공개 키 인프라에서 서버에 서버 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="abf04-122">서버에 서버 인증서가 설치 되어 있지 않으면이 옵션을 사용할 수 없으며 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="abf04-123">네트워크 서비스 계정에 사용 중인 인증서에 대 한 읽기 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="abf04-124">**TCP 포트 구성** 페이지에서 표준 포트 (554)를 사용 하려면 **기본 포트 사용 (554)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="abf04-125">사용자 지정 포트를 지정 하려면 **사용자 지정 포트 사용**을 선택 하 고 제공 된 필드에서 포트 번호를 지정한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="abf04-126">**참고**  보안 되지 않은 시나리오에서 서버를 설치 하는 경우 기본 포트 (554)를 사용 하거나 사용자 지정 포트를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="abf04-127">**콘텐츠 루트** 페이지에서 SFT 파일이 저장 되는 대상 컴퓨터의 위치를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="abf04-128">**참고**  가상 응용 프로그램 스트리밍 서버의 HTTP 또는 RTSP 포트가 이미 할당 된 경우 새 포트를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="abf04-129">원하는 포트를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="abf04-130">**고급 설정** 화면에서 다음 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="abf04-131">최대 클라이언트 연결</span><span class="sxs-lookup"><span data-stu-id="abf04-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="abf04-132">연결 시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="abf04-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="abf04-133">RTSP 스레드 풀 크기</span><span class="sxs-lookup"><span data-stu-id="abf04-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="abf04-134">RTSP 시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="abf04-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="abf04-135">코어 프로세스 수</span><span class="sxs-lookup"><span data-stu-id="abf04-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="abf04-136">코어 시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="abf04-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="abf04-137">사용자 인증 사용</span><span class="sxs-lookup"><span data-stu-id="abf04-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="abf04-138">사용자 권한 부여 사용</span><span class="sxs-lookup"><span data-stu-id="abf04-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="abf04-139">캐시 블록 크기 (KB)</span><span class="sxs-lookup"><span data-stu-id="abf04-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="abf04-140">최대 캐시 크기 (MB)</span><span class="sxs-lookup"><span data-stu-id="abf04-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="abf04-141">**참고**  App-v 스트리밍 서버는 NTFS 파일 시스템 권한을 사용 하 여 콘텐츠 공유 아래에 있는 응용 프로그램에 대 한 액세스를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="abf04-142">**사용자 인증** 사용 및 **사용자 권한 부여** 를 사용 하 여 서버에서 acl (액세스 제어 목록)을 확인 하 고 적용할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="abf04-143">**프로그램 설치 준비** 페이지에서 설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="abf04-144">**설치 마법사를 완료** 한 화면에서 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="abf04-145">**중요**  설치를 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="abf04-146">상태 메시지가 Windows 바탕 화면 알림 영역 위에 깜박입니다. 설치에 성공 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="abf04-147">메시지가 표시 되 면 컴퓨터를 다시 시작할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="abf04-148">그러나 시스템 성능을 최적화 하려면 컴퓨터를 다시 시작 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="abf04-149">설치 해야 하는 각 가상 응용 프로그램 서버에 대해 1 ~ 12 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf04-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="abf04-150">관련 항목</span><span class="sxs-lookup"><span data-stu-id="abf04-150">Related topics</span></span>


[<span data-ttu-id="abf04-151">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="abf04-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





