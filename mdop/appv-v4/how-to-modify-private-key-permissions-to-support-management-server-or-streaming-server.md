---
title: Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법
description: Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817028"
---
# <span data-ttu-id="6c3b5-103">Management Server 또는 Streaming Server를 지원하기 위해 사용 권한을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="6c3b5-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="6c3b5-104">더 안전한 App-v 설치를 지원 하려면 다음 절차를 사용 하 여 Windows Server2003 또는 Windows Server2008에서 개인 키를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="6c3b5-105">개인 키의 사용 권한을 수정 하려면 Windows Server2003 리소스 키트 도구를 사용 하면 `WinHttpCertCfg.exe` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="6c3b5-106">Windows Server2003의 경우이 절차를 수행 하려면이 문서에 나열 된 필수 구성 요소를 충족 하는 인증서가 App-v 관리 또는 스트리밍 서버를 설치 하려는 컴퓨터에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="6c3b5-107">도구 사용에 대 한 추가 정보 `WinHttpCertCfg.exe` 는에서 확인할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="6c3b5-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="6c3b5-108">Windows Server2008에서 개인 키의 Acl을 변경 하는 프로세스는 훨씬 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="6c3b5-109">인증서의 사용자 인터페이스를 사용 하 여 개인 키 사용 권한을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="6c3b5-110">**참고**  기본 보안 컨텍스트는 네트워크 서비스입니다. 그러나 도메인 계정은 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="6c3b5-111">Windows Server2003에서 개인 키를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="6c3b5-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="6c3b5-112">앱-V 관리 또는 스트리밍 서버가 되는 컴퓨터에서 명령 프롬프트에 다음 명령을 입력 하 여 특정 인증서에 할당 된 현재 사용 권한을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="6c3b5-113">필요한 경우 관리 또는 스트리밍 서비스에 사용 되는 보안 컨텍스트에 대 한 읽기 권한을 제공 하도록 인증서의 사용 권한을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="6c3b5-114">인증서에 대 한 사용 권한을 나열 하 여 보안 컨텍스트가 적절 하 게 추가 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="6c3b5-115">Windows Server2008에서 개인 키를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="6c3b5-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="6c3b5-116">*로컬 컴퓨터* 인증서 저장소를 대상으로 하는 *인증서* 스냅인을 사용 하 여 MMC (Microsoft Management Console)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="6c3b5-117">MMC를 확장 하 고 **개인 키 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="6c3b5-118">**보안** 탭에서 **읽기** 권한이 있는 **네트워크 서비스** 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c3b5-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="6c3b5-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6c3b5-119">Related topics</span></span>


[<span data-ttu-id="6c3b5-120">인증서를 구성하여 App-V Management Server 또는 Streaming Server 지원</span><span class="sxs-lookup"><span data-stu-id="6c3b5-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="6c3b5-121">인증서를 구성하여 보안 스트리밍 지원</span><span class="sxs-lookup"><span data-stu-id="6c3b5-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





