---
title: App-V 웹 관리 서비스를 지원하기 위해 인증서 구성
description: App-V 웹 관리 서비스를 지원하기 위해 인증서 구성
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821888"
---
# <span data-ttu-id="d1a0e-103">App-V 웹 관리 서비스를 지원하기 위해 인증서 구성</span><span class="sxs-lookup"><span data-stu-id="d1a0e-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="d1a0e-104">보안 통신을 위해 SSL 기반 연결을 지원 하도록 App-v 웹 관리 서비스를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="d1a0e-105">이 프로세스를 실행 하려면 관리 서비스를 설치 하는 웹 서버 또는 컴퓨터에 서비스 또는 컴퓨터에 대 한 인증서가 발급 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="d1a0e-106">다음 시나리오는이 용도로 인증서를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="d1a0e-107">회사 인프라에는 컴퓨터에 자동으로 인증서를 발급 하는 PKI (공개 키 인프라)가 이미 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="d1a0e-108">회사 인프라는 이미 PKI를 보유 하 고 있지만, 컴퓨터에 자동으로 인증서를 발급 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="d1a0e-109">회사 인프라에는 현재 PKI가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="d1a0e-110">앞의 각 시나리오에서 인증서를 가져오는 방법은 서로 다르지만 결과는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="d1a0e-111">관리자는 IIS 기본 웹 사이트에 인증서를 할당 하 고 보안 통신을 요구 하도록 App-v 웹 관리 서비스를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="d1a0e-112">**중요**  인증서 이름은 서버 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="d1a0e-113">인증서의 일반 이름에 Fqdn (정규화 된 도메인 이름)을 사용 하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="d1a0e-114">앱-V는 IIS 서버를 사용 하 여 다른 인프라 구성을 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="d1a0e-115">HTTPS를 지원 하도록 IIS 서버를 구성 하는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151972> 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="d1a0e-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d1a0e-116">Related topics</span></span>


[<span data-ttu-id="d1a0e-117">더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d1a0e-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





