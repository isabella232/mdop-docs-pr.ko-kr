---
title: 안전하게 App-V Management Server 또는 Streaming Server 설치
description: 안전하게 App-V Management Server 또는 Streaming Server 설치
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816328"
---
# <span data-ttu-id="e3080-103">안전하게 App-V Management Server 또는 Streaming Server 설치</span><span class="sxs-lookup"><span data-stu-id="e3080-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="e3080-104">이 섹션의 항목에서는 향상 된 보안 버전의 App-v 관리 서버 또는 App-v 스트리밍 서버를 설치 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="e3080-105">**참고**  향상 된 보안을 사용 하도록 App-v 관리 또는 스트리밍 서버 설치 또는 구성 (예: 전송 계층 보안 또는 TLS) 하려면 x.509 V3 인증서가 App-v Server에 프로 비전 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="e3080-106">보안 관리 또는 스트리밍 서버를 설치 또는 구성 하려고 준비 하는 경우 다음 기술 요구 사항을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3080-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="e3080-107">인증서가 유효해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-107">The certificate must be valid.</span></span> <span data-ttu-id="e3080-108">인증서가 유효 하지 않으면 클라이언트가 연결을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="e3080-109">인증서에는 올바른 EKU ( *확장 된 키 사용* ) (서버 인증 (OID 1.3.6.1.5.5.7.3.1)가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="e3080-110">인증서에이 EKU가 포함 되어 있지 않으면 클라이언트가 연결을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="e3080-111">인증서의 FQDN (정규화 된 도메인 이름)이 설치 된 서버와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="e3080-112">예를 들어 클라이언트를 호출 하 `RTSPS://Myserver.mycompany.com/content/MyApp.sft` 고 인증서 **발급 대상** 필드를로 설정한 경우 `Server1.mycompany.com` 클라이언트는 서버에 연결 되지 않고 세션이 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="e3080-113">장애가 사용자에 게 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="e3080-114">**참고**  네트워크 부하 분산 클러스터에서 App-v를 사용 하는 경우 RTSPS를 지원 하기 위해 San (주체 대체 이름)을 사용 하 여 인증서를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="e3080-115">CA (인증 기관)를 구성 하 고 San을 사용 하 여 인증서를 만드는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=133228> 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3080-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="e3080-116">클라이언트와 서버는 루트 CA를 신뢰 해야 하며, 서버에 연결 되는 인증서를 앱-V 서버에 발급 하는 CA를 신뢰할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="e3080-117">그렇지 않으면 클라이언트가 연결을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="e3080-118">인증서의 개인 키에 대 한 사용 권한이 변경 되어 앱-V 서비스 계정이 인증서에 액세스할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="e3080-119">기본적으로 App-v는 네트워크 서비스 계정을 사용 하며 기본적으로 네트워크 서비스 계정에는 개인 키에 액세스할 수 있는 권한이 없으므로 보안 연결이 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="e3080-120">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="e3080-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="e3080-121">인증서를 구성하여 보안 스트리밍 지원</span><span class="sxs-lookup"><span data-stu-id="e3080-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="e3080-122">보안 스트리밍을 지 원하는 인증서를 가져오고, 구성 하 고, 설치 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="e3080-123">Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="e3080-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="e3080-124">Windows Server2003 및 Windows Server2008에서 키를 수정 하는 데 사용할 수 있는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="e3080-125">인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원</span><span class="sxs-lookup"><span data-stu-id="e3080-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="e3080-126">네트워크 부하 분산 환경용 인증서 구성에 대 한 정보를 포함 하 여 App-v 관리 또는 스트리밍 서버의 인증서를 구성 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3080-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





