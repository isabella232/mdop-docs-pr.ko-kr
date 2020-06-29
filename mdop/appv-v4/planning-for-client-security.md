---
title: 클라이언트 보안 계획
description: 클라이언트 보안 계획
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815933"
---
# <span data-ttu-id="631b0-103">클라이언트 보안 계획</span><span class="sxs-lookup"><span data-stu-id="631b0-103">Planning for Client Security</span></span>


<span data-ttu-id="631b0-104">App-v 클라이언트는 이전 버전의 제품에는 없는 몇 가지 보안 향상 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-104">The App-V Client provides several security enhancements that were not present in previous versions of the product.</span></span> <span data-ttu-id="631b0-105">이러한 변경 사항은 설치 후 클라이언트 설정의 이후 구성을 통해 향상 된 보안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-105">These changes provide improved security after installation and through later configuration of the client settings.</span></span> <span data-ttu-id="631b0-106">이 항목에서는 이러한 개선 사항 중 몇 가지를 설명 하 고 계획 프로세스 중에 고려해 야 하는 중요 한 몇 가지 보안 관련 구성 설정을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-106">This topic describes some of those enhancements and identifies several important security-related configuration settings that you should consider during your planning process.</span></span> <span data-ttu-id="631b0-107">가상 응용 프로그램은 여전히 실행 되는 것 이므로 권한이 없는 사용자가 이러한 자산을 훼손 시킬 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-107">It is important to remember that virtual applications are still executables, so you must ensure that these assets cannot be tampered with by unauthorized people.</span></span> <span data-ttu-id="631b0-108">이러한 이유로 OSD (Open Software Descriptor) 파일 캐시는이 항목의 뒷부분에 설명 된 대로 보호 되며, RTSPS, HTTPS 및 IPsec을 사용 하 여 게시와 스트리밍을 보호 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-108">For this reason, the Open Software Descriptor (OSD) file cache is protected as described later in this topic, and we strongly recommend that you use RTSPS, HTTPS, and IPsec to protect publishing and streaming.</span></span>

## <span data-ttu-id="631b0-109">App-v 클라이언트 보안</span><span class="sxs-lookup"><span data-stu-id="631b0-109">App-V Client Security</span></span>


<span data-ttu-id="631b0-110">기본적으로 App-v 클라이언트는 사용자가 게시 새로 고침을 수행 하 고 응용 프로그램을 시작할 수 있도록 허용 하는 데 필요한 최소 사용 권한으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-110">By default, at installation the App-V client is configured with the minimum permissions required to allow a user to perform a publishing refresh and to start applications.</span></span> <span data-ttu-id="631b0-111">App-v 클라이언트에 제공 되는 기타 보안 향상 기능에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-111">Other security enhancements provided in the App-V client include the following:</span></span>

-   <span data-ttu-id="631b0-112">기본적으로 OSD 파일 캐시는 관리자와 게시 새로 고침 프로세스를 사용 하 여 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-112">By default, the OSD file cache can be updated only by administrators and by using the publishing refresh process.</span></span>

-   <span data-ttu-id="631b0-113">로그 파일 (sftlog.txt)은 클라이언트에 대 한 로컬 관리 액세스 권한이 있는 계정 으로만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-113">The log file (sftlog.txt) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="631b0-114">이제 로그 파일의 크기가 최대입니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-114">The log file now has a maximum size.</span></span>

### <span data-ttu-id="631b0-115">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="631b0-115">File Type Associations</span></span>

<span data-ttu-id="631b0-116">기본적으로 클라이언트 설치는 OSD 파일에 대 한 FTAs (파일 형식 연결)를 등록 하 여 사용자가 게시 된 바로 가기 대신 OSD 파일에서 직접 응용 프로그램을 시작할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-116">By default, the installation of the client registers file type associations (FTAs) for OSD files, which enables users to start applications directly from OSD files instead of the published shortcuts.</span></span> <span data-ttu-id="631b0-117">로컬 관리자 권한이 있는 사용자가 악성 코드를 포함 하는 OSD 파일을 전자 메일 또는 웹 사이트에서 다운로드 하는 경우, 사용자는 클라이언트가 **응용 프로그램 추가** 권한을 제한 하도록 설정 된 경우에도 osd 파일을 열고 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-117">If a user with local administrator rights receives an OSD file containing malicious code, either in e-mail or downloaded from a Web site, the user can open the OSD file and start the application even if the client has been set to restrict the **Add Application** permission.</span></span> <span data-ttu-id="631b0-118">이 위험을 줄이기 위해 OSD를 위해 FTAs를 등록 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-118">You can unregister the FTAs for the OSD to reduce this risk.</span></span> <span data-ttu-id="631b0-119">또한 전자 메일 시스템 및 방화벽에서이 확장을 차단 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-119">Also, consider blocking this extension in the e-mail system and at the firewall.</span></span> <span data-ttu-id="631b0-120">확장을 차단 하도록 Outlook을 구성 하는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=133278> 하세요.</span><span class="sxs-lookup"><span data-stu-id="631b0-120">For more information about configuring Outlook to block extensions, see <https://go.microsoft.com/fwlink/?LinkId=133278>.</span></span>

**<span data-ttu-id="631b0-121">보안 참고:</span><span class="sxs-lookup"><span data-stu-id="631b0-121">Security Note:</span></span>**

<span data-ttu-id="631b0-122">App-v 버전 4.6으로 시작 하는 경우, 클라이언트를 새로 설치 하는 동안 OSD 파일에 대 한 파일 형식 연결이 더 이상 만들어지지 않지만, App-v 클라이언트의 버전 4.2 또는 4.5에서 업그레이드 하는 동안 기존 설정이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-122">Starting with App-V version4.6, the file type association is no longer created for OSD files during a new installation of the client, although the existing settings will be maintained during an upgrade from version 4.2 or 4.5 of the App-V client.</span></span> <span data-ttu-id="631b0-123">어떤 이유로 든 파일 형식 연결을 만드는 것이 중요 한 경우 다음과 같이 레지스트리 키를 만들고 해당 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-123">If for any reason it is essential to create the file type association, you can create the following registry keys and set their values as shown:</span></span>

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### <span data-ttu-id="631b0-124">권한 부여</span><span class="sxs-lookup"><span data-stu-id="631b0-124">Authorization</span></span>

<span data-ttu-id="631b0-125">설치 하는 동안 **Requireauthorizationifcached** 매개 변수를 사용 하 여 사용자가 응용 프로그램을 시작 하려고 할 때 서버에서 인증을 요구 하도록 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-125">During installation, you can use the **RequireAuthorizationIfCached** parameter to configure the client to require authorization from the server when the user tries to start an application.</span></span> <span data-ttu-id="631b0-126">이 매개 변수를 설정 하는 방법은 신중 하 게 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-126">You should consider carefully how to set this parameter.</span></span> <span data-ttu-id="631b0-127">어떤 이유로 든 App-v 서버를 사용할 수 없는 경우 응용 프로그램은이 매개 변수의 가장 최근 저장 된 상태를 사용 하 여 응용 프로그램에 대 한 사용자 액세스를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-127">If the App-V server is unavailable for any reason, the application will use the most recent stored state of this parameter to control user access to the application.</span></span> <span data-ttu-id="631b0-128">사용자가 App-v server를 사용할 수 없게 되기 전에 응용 프로그램을 성공적으로 실행 하지 않은 경우, 서버와 통신 하 고 권한 부여를 받을 때까지 응용 프로그램을 시작할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-128">If the user has not launched the application successfully before the App-V server becomes unavailable, they will not be able to launch the application until they can communicate with the server and receive authorization.</span></span> <span data-ttu-id="631b0-129">그러나 클라이언트에 권한이 필요 하지 않고 서버를 사용할 수 없는 경우에는 매개 변수를 설정 하는 경우, 이전에 캐시 된 모든 응용 프로그램을 권한이 있는지 여부에 관계 없이 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-129">However, if you set the parameter so that the client does not require authorization and if the server is unavailable, all previously cached applications can be started whether authorized or not.</span></span> <span data-ttu-id="631b0-130">또한 사용 권한을 통해 오프 라인 모드에서 클라이언트를 변경할 수 있는 권한이 있거나 사용자가 로컬 관리자 인 경우 사용자는 모든 캐시 된 패키지를 앱-V 인프라를 사용할 수 없는 것 처럼 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-130">Also, if the user has permission to change the client to Work Offline mode through permissions or if the user is a local administrator, the user would be able to open all cached packages as if the App-V infrastructure was unavailable.</span></span>

### <span data-ttu-id="631b0-131">바이러스 백신 검사</span><span class="sxs-lookup"><span data-stu-id="631b0-131">Antivirus Scanning</span></span>

<span data-ttu-id="631b0-132">App-v 클라이언트 컴퓨터에서 실행 되는 바이러스 백신 소프트웨어는 가상 환경에서 감염 된 파일을 검색 하 고 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-132">Antivirus software running on an App-V Client computer can detect and report an infected file in the virtual environment.</span></span> <span data-ttu-id="631b0-133">그러나 파일을 치료 하는 것은 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-133">However, it cannot disinfect the file.</span></span> <span data-ttu-id="631b0-134">가상 환경에서 바이러스가 검색 되는 경우 바이러스 백신 소프트웨어는 실제 패키지가 아닌 캐시에서 구성 된 격리 또는 복구 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-134">If a virus is detected in the virtual environment, the antivirus software would perform the configured quarantine or repair operation in the cache, not in the actual package.</span></span> <span data-ttu-id="631b0-135">Sftfs .fd 파일에 대 한 예외를 사용 하 여 바이러스 백신 소프트웨어를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-135">Configure the antivirus software with an exception for the sftfs.fsd file.</span></span> <span data-ttu-id="631b0-136">이 파일은 앱-V 클라이언트에 패키지를 저장 하는 캐시 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-136">This file is the cache file that stores packages on the App-V Client.</span></span>

**<span data-ttu-id="631b0-137">보안 참고:</span><span class="sxs-lookup"><span data-stu-id="631b0-137">Security Note:</span></span>**

<span data-ttu-id="631b0-138">프로덕션 환경에 배포 된 응용 프로그램이 나 패키지에서 바이러스가 검색 되는 경우에는 응용 프로그램 또는 패키지를 바이러스를 사용 하지 않는 버전으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-138">If a virus is detected in an application or package deployed in the production environment, replace the application or package with a virus-free version.</span></span>

## <span data-ttu-id="631b0-139">클라이언트와 서버 간의 통신</span><span class="sxs-lookup"><span data-stu-id="631b0-139">Communication Between Client and Server</span></span>


<span data-ttu-id="631b0-140">게시 새로 고침 및 패키지 스트리밍은 클라이언트-서버 통신과 관련 된 보안 고려 사항이 중요 한 영역 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-140">Publishing refreshes and package streaming are also areas where security considerations relating to client-server communication are important.</span></span>

### <span data-ttu-id="631b0-141">게시 새로 고침</span><span class="sxs-lookup"><span data-stu-id="631b0-141">Publishing Refresh</span></span>

<span data-ttu-id="631b0-142">클라이언트가 게시 새로 고침을 수행 하기 위해 서버와 통신 하는 경우 로그온 한 사용자의 자격 증명을 사용 하 여 응용 프로그램 패키지에 대 한 정보를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-142">When the client communicates with the server to perform a publishing refresh, it uses the credentials of the logged on user to request information about the application packages.</span></span> <span data-ttu-id="631b0-143">전송 중에는 어떠한 게시 정보도 훼손 될 수 없도록 App-v 클라이언트와 App-v 관리 서버 간에 발생 하는 통신을 보호 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-143">You should secure the communication that occurs between the App-V client and App-V Management Server to ensure that none of the publishing information can be tampered with in transit.</span></span> <span data-ttu-id="631b0-144">이 작업은 RTSPS/HTTPS를 사용 하는 향상 된 보안 옵션을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-144">This is done by using the Enhanced Security option, which will use RTSPS/HTTPS.</span></span> <span data-ttu-id="631b0-145">.ICO 및 OSD 파일이 저장 되는 위치와 클라이언트 간 통신은 SMB/CIFS 공유 및 IIS 서버용 HTTPS에 대해 IPsec을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-145">Communication between the Client and the location where the ICO and OSD files are stored should use IPsec for SMB/CIFS shares and HTTPS for an IIS server.</span></span>

<span data-ttu-id="631b0-146">**참고**  IIS를 사용 하 여 .ICO 및 OSD 파일을 게시 하는 경우 OSD = TXT에 대 한 MIME 형식을 구성 합니다. 그렇지 않은 경우에는 IIS가 .ICO 및 OSD 파일을 클라이언트에 제공 하는 것을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-146">**Note** If you are using IIS to publish the ICO and OSD files, configure a MIME type for OSD=TXT; otherwise, IIS will refuse to serve the ICO and OSD files to clients.</span></span>

 

### <span data-ttu-id="631b0-147">패키지 스트리밍</span><span class="sxs-lookup"><span data-stu-id="631b0-147">Package Streaming</span></span>

<span data-ttu-id="631b0-148">사용자가 처음으로 응용 프로그램을 시작 하거나 클라이언트에 자동 로드 하는 매개 변수가 설정 된 경우 응용 프로그램 패키지는 서버에서 클라이언트 캐시로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-148">When a user launches an application for the first time, or if auto-loading parameters have been set on the client, the application package is streamed from a server to the client cache.</span></span> <span data-ttu-id="631b0-149">이 프로세스는 RTSP/RTSPS, HTTP/HTTPS, SMB/CIFS 프로토콜을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-149">This process supports the RTSP/RTSPS, HTTP/HTTPS, and SMB/CIFS protocols.</span></span> <span data-ttu-id="631b0-150">OSD 파일은 **ApplicationSourceRoot** 또는 **overrideurl** 설정이 클라이언트에 구성 되어 있지 않은 경우 사용 되는 프로토콜을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-150">The OSD files control which protocols are used, unless the **ApplicationSourceRoot** or **OverrideURL** setting has been configured on the clients.</span></span> <span data-ttu-id="631b0-151">SMB/CIFS에 대해 RTSPS, HTTPS 또는 IPsec을 통해 통신을 수행 하 여 더 높은 수준의 보안을 구현 하도록 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-151">You should configure communication to occur over RTSPS, HTTPS, or IPsec for SMB/CIFS to achieve higher levels of security.</span></span> <span data-ttu-id="631b0-152">사용할 통신 방법을 선택 하는 방법에 대 한 자세한 내용은의 App-v 계획 및 배포 가이드를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=122063> .</span><span class="sxs-lookup"><span data-stu-id="631b0-152">For more information about choosing which communication method to use, see the App-V Planning and Deployment Guide at <https://go.microsoft.com/fwlink/?LinkId=122063>.</span></span>

<span data-ttu-id="631b0-153">**참고**  IIS를 사용 하 여 패키지 (SFT 파일)를 게시 하는 경우 SFT = Binary에 대 한 MIME 형식을 구성 합니다. 그렇지 않으면 IIS가 클라이언트에 SFT 파일을 제공 하는 것을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-153">**Note** If you are using IIS to publish packages (SFT files), configure a MIME type for SFT=Binary; otherwise, IIS will refuse to serve the SFT files to clients.</span></span>

 

### <span data-ttu-id="631b0-154">로밍 프로필 및 폴더 리디렉션</span><span class="sxs-lookup"><span data-stu-id="631b0-154">Roaming Profiles and Folder Redirection</span></span>

<span data-ttu-id="631b0-155">App-v 시스템은 usrvol \\ _sftfs \ _v1 installer.pkg 파일에 패키지에 대 한 사용자 관련 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-155">The App-V system stores user-specific changes to packages in the usrvol\_sftfs\_v1.pkg file.</span></span> <span data-ttu-id="631b0-156">이 파일은 사용자 프로필의 응용 프로그램 데이터 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-156">This file is located in the Application Data folder of a user’s profile.</span></span> <span data-ttu-id="631b0-157">프로필 또는 리디렉션된 응용 프로그램 데이터 폴더가 클라이언트와 서버 간에 전송 되므로 IPsec을 사용 하 여 통신을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-157">Because the profile or a redirected Application Data folder is transferred between the client and the server, use IPsec to secure the communication.</span></span>

## <span data-ttu-id="631b0-158">인터넷 연결 클라이언트에 대 한 고려 사항</span><span class="sxs-lookup"><span data-stu-id="631b0-158">Considerations for Internet-Facing Clients</span></span>


<span data-ttu-id="631b0-159">인터넷 연결 클라이언트의 경우 클라이언트가 도메인에 가입 되어 있는지 아니면 도메인에 가입 되어 있지 않은 지 고려 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-159">For Internet-facing clients, it is important to consider whether the client is domain joined or non-domain joined.</span></span>

### <span data-ttu-id="631b0-160">도메인에 가입 된 클라이언트</span><span class="sxs-lookup"><span data-stu-id="631b0-160">Domain Joined Client</span></span>

<span data-ttu-id="631b0-161">기본적으로 App-v 클라이언트는 Active Directory 도메인 서비스가 인트라넷의 인증 및 권한 부여를 위해 발급 한 Kerberos 티켓을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-161">By default, App-V Clients use Kerberos tickets that were issued by Active Directory Domain Services for authentication and authorization on the intranet.</span></span> <span data-ttu-id="631b0-162">이러한 Kerberos 티켓은 기본적으로 10 시간 동안 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-162">These Kerberos tickets are valid for 10 hours by default.</span></span> <span data-ttu-id="631b0-163">클라이언트가 티켓을 새로 고치기 위해 도메인 컨트롤러에 연결할 수 없는 경우에도 클라이언트는이 티켓을 사용 하 여 티켓이 유효한 경우에만 앱-V server에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-163">The client will use this ticket to access the App-V server for as long as the ticket is valid, even if the computer is unable to connect to the domain controller to refresh the ticket.</span></span> <span data-ttu-id="631b0-164">Kerberos 티켓이 만료 되는 경우 App-v 클라이언트는 NTLM 인증으로 되돌아가고 사용자의 캐시 된 자격 증명을 사용 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-164">If the Kerberos ticket expires, the App-V client will revert to NTLM authentication and use the user’s cached credentials.</span></span>

### <span data-ttu-id="631b0-165">비도메인 가입 클라이언트</span><span class="sxs-lookup"><span data-stu-id="631b0-165">Non-Domain Joined Client</span></span>

<span data-ttu-id="631b0-166">사용자가 홈 기반이 고 컴퓨터가 회사 도메인에 가입 되어 있지 않으면 앱-V가 제공 하는 응용 프로그램을 계속 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-166">If a user is home-based and the computer is not joined to the company domain, App-V can still support delivering applications.</span></span> <span data-ttu-id="631b0-167">게시 새로 고침을 수행 하 고 응용 프로그램을 시작 하기 위해 사용자를 인증 하 고 권한을 부여 하려면 클라이언트 컴퓨터에서 사용자 계정을 구성 하 여 App-v 환경에 대 한 액세스 권한이 있는 사용자 이름 및 암호를 저장 하 고 응용 프로그램에 적절 한 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="631b0-167">To authenticate and authorize a user to perform a publishing refresh and to start applications, configure the user account on the client computer to store the user name and password that has access to the App-V environment and to provide appropriate permissions to the applications.</span></span>

## <span data-ttu-id="631b0-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="631b0-168">Related topics</span></span>


[<span data-ttu-id="631b0-169">보안 및 보호 계획</span><span class="sxs-lookup"><span data-stu-id="631b0-169">Planning for Security and Protection</span></span>](planning-for-security-and-protection.md)

 

 





