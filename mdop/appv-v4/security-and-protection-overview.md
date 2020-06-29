---
title: 보안 및 보호 개요
description: 보안 및 보호 개요
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815658"
---
# <span data-ttu-id="67ae2-103">보안 및 보호 개요</span><span class="sxs-lookup"><span data-stu-id="67ae2-103">Security and Protection Overview</span></span>


<span data-ttu-id="67ae2-104">Microsoft Application Virtualization 4.5는 보다 안전한 배포 전략을 계획 하 고 구현 하는 데 도움이 되는 다음과 같은 향상 된 보안 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="67ae2-105">이제 응용 프로그램 가상화는 x.509 V3 인증서를 사용 하 여 TLS (Transport Layer Security)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="67ae2-106">서버 인증서가 계획 된 응용 프로그램 가상화 관리 또는 스트리밍 서버로 프로 비전 되 고 나면 기본적으로 포트 322에서 RTSPS 프로토콜을 사용 하 여 설치가 안전 하 게 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="67ae2-107">RTSPS를 사용 하면 응용 프로그램 가상화 서버와 응용 프로그램 가상화 클라이언트 간의 통신이 서명 및 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="67ae2-108">응용 프로그램 가상화 서버를 설치 하는 동안 서버에 할당 된 인증서가 없는 경우 통신은 포트 554을 통해 RTSP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="67ae2-109">보안 참고:</span><span class="sxs-lookup"><span data-stu-id="67ae2-109">Security Note:</span></span>**

    <span data-ttu-id="67ae2-110">서버를 안전 하 게 설치할 수 있도록 하려면 RTSPS를 사용 하도록 구성 된 모든 패키지가 있는 경우에도 RTSP 포트를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="67ae2-111">서버를 설치한 후 서버에 보안 인증서를 추가 하는 경우 서버에서 인증서를 감지 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="67ae2-112">보안 인증서 검색을 위해 인증서를 추가한 후 서버를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="67ae2-113">클라이언트는 서버와 동일한 프로토콜 및 포트를 사용 하도록 구성 되어 있어야 하며 그렇지 않으면 서버와 통신 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="67ae2-114">또한 클라이언트는 인증서의 발급자를 신뢰 하 고 신뢰할 수 있는 루트 저장소의 몇 가지 기본 공급자와 함께 제공 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="67ae2-115">자체 서명 된 인증서를 사용할 수는 있지만 클라이언트를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="67ae2-116">스트리밍에 HTTPS 프로토콜을 사용 하도록 IIS 서버를 구성할 때는 IIS 서버에서 SSL (Secure Sockets layer)을 설정 하 고 서버에 대 한 인증서를 프로 비전 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="67ae2-117">또한 클라이언트는 서버 인증서를 발급 한 루트 인증 기관을 신뢰 하도록 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="67ae2-118">Kerberos 인증이 기본 인증 메커니즘으로 Microsoft Application Virtualization에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="67ae2-119">이전 버전은 인증을 위해 NTLM V2에 의존 했습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="67ae2-120">Kerberos 인증을 사용 하면 클라이언트와 응용 프로그램 가상화 서버 간의 통신 보안을 강화할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="67ae2-121">클라이언트에서 연결이 시작 되 면 Application Virtualization 서버는 KDC (키 배포 센터)를 사용 하 여 세션 티켓을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="67ae2-122">서버 인증서를 사용 하 고 RTSPS 또는 HTTPS 프로토콜을 사용 하는 데 대 한 지원 때문에 이제 회사 네트워크 외부의 클라이언트를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="67ae2-123">이렇게 하면 모바일 사용자가 응용 프로그램 가상화 프로 비전 된 응용 프로그램을 시작 하기 전에 회사 네트워크 (VPN, RAS 등)에 대 한 보안 연결을 설정 하지 않아도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="67ae2-124">고려해 야 할 다른 중요 보안 고려 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="67ae2-125">항상 서버를 완전히 업데이트 하 고 보호 하도록 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="67ae2-126">인증서를 추가 하 여 응용 프로그램 가상화 관리 서버에 더욱 안전한 통신을 사용 하도록 설정 하려면 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="67ae2-127">인증서를 추가할 사용자는 인증서 저장소가 있는 서버의 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="67ae2-128">서버 서비스를 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-128">The server service must be started.</span></span>

    -   <span data-ttu-id="67ae2-129">관리 서버의 포트 139이 웹 서비스 서버 SIP에 열려 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="67ae2-130">Acl (액세스 제어 목록)을 사용 하 여 응용 프로그램 패키지 및 모든 패키지 파일이 보호 되 고 무단으로 변경 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="67ae2-131">특정 계정에만 액세스할 수 있도록 패키지를 저장 하는 위치 또는 폴더에 대 한 액세스를 Acl에서 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="67ae2-132">예를 들어 IPsec를 사용 하 여 응용 프로그램 가상화 관리 서버와 데이터베이스 간의 채널이 보안 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="67ae2-133">패키지가 SAN 또는 NAS에 저장 되어 있는 경우 중앙 저장소 장치와 응용 프로그램 가상화 서버 간의 연결이 보호 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="67ae2-134">HTTPS 또는 IPsec 등의 프로토콜을 사용 하 여 클라이언트에 대 한 모든 통신 채널 (게시 서버, 응용 프로그램 가상화 서버, OSD 및 .ICO 파일 경로)에 대 한 연결을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="67ae2-135">사용자가 패키지를 임의로 변경할 수 없도록 클라이언트 사용 권한을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="67ae2-136">특히, 여러 사용자와 공유 되는 원격 데스크톱 세션 호스트 (RDSession Host) 서버와 같은 시스템에서 패키지를 추가 하거나 업데이트 하는 데 필요한 권한을 사용자에 게 부여 하지 않는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="67ae2-137">서버 관리 콘솔이 올바르게 작동 하려면 도메인 또는 포리스트 환경에서 Kerberos 인증을 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="67ae2-138">이 소프트웨어 릴리스는 동일한 컴퓨터에서 Kerberos 기반 RTSP 서버와 Microsoft NTLM 전용 IIS 서버 호스팅을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="67ae2-139">동일한 컴퓨터에서 RTSP 서버와 IIS 서버를 호스팅하려면 IIS 서버에서 SPN을 제거 하 고 NTLM 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ae2-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="67ae2-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="67ae2-140">Related topics</span></span>


[<span data-ttu-id="67ae2-141">Application Virtualization 시스템 배포 계획</span><span class="sxs-lookup"><span data-stu-id="67ae2-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





