---
title: 보안 스트리밍을 위해 IIS 구성
description: 보안 스트리밍을 위해 IIS 구성
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821883"
---
# <span data-ttu-id="24fc5-103">보안 스트리밍을 위해 IIS 구성</span><span class="sxs-lookup"><span data-stu-id="24fc5-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="24fc5-104">Microsoft App-v (Application Virtualization) 버전 4.5에서 HTTP 및 HTTPS를 사용 하 여 응용 프로그램 패키지를 App-v 클라이언트에 스트리밍하는 프로토콜을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="24fc5-105">이 옵션을 사용 하면 조직에서 IIS가 일반적으로 제공 하는 추가 확장성을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="24fc5-106">IIS를 스트리밍 서버로 사용할 때 HTTP 대신 HTTPS를 사용 하 여 클라이언트와 서버 간의 통신을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="24fc5-107">**참고**  파일 서버에서 응용 프로그램을 스트림할 경우 응용 프로그램 패키지에 대 한 통신의 보안을 강화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="24fc5-108">이는 IPsec을 사용 하 여 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="24fc5-109">자세한 내용은 TechNet 라이브러리의 다음 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24fc5-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="24fc5-110">Windows Server2003의 경우</span><span class="sxs-lookup"><span data-stu-id="24fc5-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="24fc5-111">Windows Server 2008의 경우</span><span class="sxs-lookup"><span data-stu-id="24fc5-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="24fc5-112">MIME 형식</span><span class="sxs-lookup"><span data-stu-id="24fc5-112">MIME Types</span></span>


<span data-ttu-id="24fc5-113">IIS를 사용 하 여 가상 응용 프로그램을 HTTP 또는 HTTPS로 스트리밍할 때 App-v를 지원 하려면 다음 MIME 형식을 IIS 서버에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="24fc5-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="24fc5-114">.OSD=TXT</span></span>

-   <span data-ttu-id="24fc5-115">. SFT = Binary</span><span class="sxs-lookup"><span data-stu-id="24fc5-115">.SFT=Binary</span></span>

<span data-ttu-id="24fc5-116">MIME 형식 추가에 대 한 지침으로 다음 KB 문서를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="24fc5-117">IIS 6.0:</span><span class="sxs-lookup"><span data-stu-id="24fc5-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="24fc5-118">IIS 7.0:</span><span class="sxs-lookup"><span data-stu-id="24fc5-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="24fc5-119">Kerberos 인증</span><span class="sxs-lookup"><span data-stu-id="24fc5-119">Kerberos Authentication</span></span>


<span data-ttu-id="24fc5-120">HTTP 또는 HTTPS 및 Kerberos 인증을 사용 하 여 .ICO, OSD 또는 SFT 파일을 스트리밍하는 경우 사용자 환경의 보안이 향상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="24fc5-121">그러나 IIS에서 Kerberos 인증을 지원 하려면 올바른 SPN (서비스 사용자 이름)을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="24fc5-122">이 `setspn.exe` 도구는 Windows Server2003에서 설치 CD의 지원 도구를 통해 사용할 수 있으며 Windows Server2008에 기본으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24fc5-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="24fc5-123">SPN을 만들려면 `setspn.exe` 도메인 관리자의 구성원으로 로그인 한 상태에서 명령 프롬프트에서 실행 합니다 (예:) `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="24fc5-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="24fc5-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="24fc5-124">Related topics</span></span>


[<span data-ttu-id="24fc5-125">보안 통신 사후 설치를 위해 Management Server 또는 Streaming Server 구성</span><span class="sxs-lookup"><span data-stu-id="24fc5-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





