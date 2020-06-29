---
title: 인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원
description: 인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821898"
---
# <span data-ttu-id="b1a9f-103">인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원</span><span class="sxs-lookup"><span data-stu-id="b1a9f-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="b1a9f-104">인증서 프로비저닝 프로세스를 완료 하 고 앱-V 설치를 지원 하도록 개인 키 사용 권한을 변경한 후에는 관리 서버 또는 스트리밍 서버의 설정을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="b1a9f-105">설치 중에 인증서를 프로 비전 하는 경우 설치 프로그램을 실행 하기 전에 마법사는 **연결 보안 모드** 화면에 인증서를 표시 하 고 기본적으로 **향상 된 보안 사용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="b1a9f-106">**참고**  이 서버에 대해 프로 비전 된 인증서가 두 개 이상 있는 경우 App-v에 대해 구성 된 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="b1a9f-107">**중요**  버전 4.2에서 버전 4.5으로 업그레이드할 때 설정에는 향상 된 보안을 **사용할**수 있는 옵션이 있습니다. 그러나이 옵션을 선택 해도 RTSP 상에 서 스트리밍이 비활성화 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="b1a9f-108">설치 후에는 관리 콘솔을 사용 하 여 RTSP를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="b1a9f-109">서비스가 클라이언트 통신에 사용할 TCP 포트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="b1a9f-110">기본 포트는 TCP 322입니다. 그러나 해당 환경의 사용자 지정 포트로 포트를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="b1a9f-111">마법사의 나머지 단계는 **향상 된 보안** 기능을 사용 하지 않고 app-v 관리 또는 스트리밍 서버를 배포 하는 것과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="b1a9f-112">NLB 환경에 대 한 인증서 구성</span><span class="sxs-lookup"><span data-stu-id="b1a9f-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="b1a9f-113">대규모 기업을 지원 하기 위해 많은 수의 연결을 지원 하기 위해 관리 서버를 NLB (네트워크 부하 분산) 클러스터에 배치 하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="b1a9f-114">여기에는 단일 관리 서버로 표시 되는 두 개 이상의 관리 서버가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="b1a9f-115">환경에서 여러 관리 서버에 대 한 NLB 클러스터를 사용 하는 경우 NLB 클러스터에 사용 되는 인증서의 고급 구성이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="b1a9f-116">App-v 인증서는 Windows Server2003를 실행 하는 컴퓨터에 구성 된 CA (인증 기관)에 제출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="b1a9f-117">SAN을 사용 하면 NLB 클러스터를 구성 하는 32 서버가 있을 수 있으므로 실제 컴퓨터 이름과 다를 수 있는 DNS (Domain Name System) 이름으로 특정 관리 서버 NLB 클러스터 호스트 이름을 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="b1a9f-118">이 구성은 NLB 클러스터를 사용 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="b1a9f-119">클라이언트가 서버에 연결 되 면 개별 서버의 FQDN을 제외한 NLB 클러스터의 FQDN (정규화 된 도메인 이름)을 사용 하 여 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="b1a9f-120">클러스터에 있는 서버 노드의 FQDN을 사용 하 여 SAN 속성을 추가 하지 않으면 인증서의 일반 이름이 서버 이름과 일치 하지 않기 때문에 모든 클라이언트 연결이 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="b1a9f-121">SAN 특성을 사용 하 여 인증서를 구성 하는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=133228> 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1a9f-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="b1a9f-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b1a9f-122">Related topics</span></span>


[<span data-ttu-id="b1a9f-123">인증서를 구성하여 보안 스트리밍 지원</span><span class="sxs-lookup"><span data-stu-id="b1a9f-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="b1a9f-124">Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b1a9f-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





