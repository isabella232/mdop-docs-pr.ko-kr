---
title: MED-V 작업의 보안 모범 사례
description: MED-V 작업의 보안 모범 사례
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825398"
---
# <span data-ttu-id="54af0-103">MED-V 작업의 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="54af0-103">Security Best Practices for MED-V Operations</span></span>


<span data-ttu-id="54af0-104">권한 있는 관리자는 MED-V 작업 영역 배포 중에 사용자의 정보를 보호 하 고 조직의 보안을 유지 하는 책임을 집니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-104">As an authorized administrator, you are responsible to protect the information of the users and maintain security of your organization during and after the deployment of MED-V workspaces.</span></span> <span data-ttu-id="54af0-105">특히 다음 문제를 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="54af0-105">In particular, consider the following issues.</span></span>

<span data-ttu-id="54af0-106">**Med-v 작업 영역에서 Internet Explorer를 사용자 지정**합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-106">**Customizing Internet Explorer in the MED-V workspace**.</span></span> <span data-ttu-id="54af0-107">이전 버전의 Windows 운영 체제와 Internet Explorer는 현재 버전 만큼 안전 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-107">Earlier versions of the Windows operating system and of Internet Explorer are not as secure as current versions.</span></span> <span data-ttu-id="54af0-108">따라서 MED-V 작업 영역의 Internet Explorer는 보안 위험이 발생할 수 있는 탐색 및 기타 작업을 방지 하도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-108">Therefore, Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span> <span data-ttu-id="54af0-109">또한 MED-V 작업 영역의 Internet Explorer에 대 한 인터넷 보안 영역 설정은 최고 수준으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-109">In addition, the Internet security zone setting for Internet Explorer in the MED-V workspace is set to the highest level.</span></span> <span data-ttu-id="54af0-110">기본적으로이 두 구성은 med-v 작업 영역 패키지를 만들 때 MED-V 작업 영역 포장기에서 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-110">By default, both of these configurations are set in the MED-V Workspace Packager when you create your MED-V workspace package.</span></span>

<span data-ttu-id="54af0-111">IEAK (Internet Explorer 관리 키트)를 사용 하거나 MED-V 작업 영역 포장기의 기본값을 변경 하 여 MED-V 작업 영역에서 Internet Explorer를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-111">By using Internet Explorer Administration Kit (IEAK) or by changing the defaults in the MED-V Workspace Packager, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="54af0-112">그러나 MED-V 작업 영역에서 Internet Explorer를 사용자 지정 하 여 보안 수준을 낮게 만드는 경우 이전 버전의 Internet Explorer에 있는 보안 위험에 조직이 노출 될 수 있다는 것을 염두에 두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-112">However, realize that if you customize Internet Explorer in the MED-V workspace in such a way as to make it less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span>

<span data-ttu-id="54af0-113">보안 관점에서 보면 MED-V 작업 영역에서 Internet Explorer를 관리 하기 위한 모범 사례는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-113">From a security perspective, best practices for managing Internet Explorer in the MED-V workspace are as follows:</span></span>

-   <span data-ttu-id="54af0-114">MED-V 작업 영역 패키지를 만들 때 MED-V 작업 영역의 Internet Explorer가 보안 위험을 초래할 수 있는 탐색 및 기타 작업을 방지 하도록 구성 된 기본 집합을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-114">When creating your MED-V workspace package, leave the defaults set so that Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span>

-   <span data-ttu-id="54af0-115">MED-V 작업 영역 패키지를 만들 때 인터넷 보안 영역의 보안 설정이 가장 높은 수준으로 유지 되도록 기본 집합을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-115">When creating your MED-V workspace package, leave the defaults set so that the security setting for the Internet security zone remains at the highest level.</span></span>

-   <span data-ttu-id="54af0-116">회사의 인트라넷 외부에 있는 도메인을 차단 하도록 엔터프라이즈 프록시 또는 Internet Explorer 콘텐츠 도우미를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-116">Configure your enterprise proxy or Internet Explorer Content Advisor to block domains that are outside your company’s intranet.</span></span>

**<span data-ttu-id="54af0-117">공유 컴퓨터의 모든 사용자에 대 한 MED-V 작업 영역 구성</span><span class="sxs-lookup"><span data-stu-id="54af0-117">Configuring a MED-V workspace for all users on a shared computer.</span></span>** <span data-ttu-id="54af0-118">공유 컴퓨터의 모든 사용자가 액세스할 수 있도록 MED-V 작업 영역을 구성할 때 해당 시스템의 모든 사용자에 게 읽기 및 쓰기 액세스 권한을 제공 하는 위치에 VHD (게스트 가상 컴퓨터)가 포함 되어 있음을 인식 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-118">When configuring a MED-V workspace so that it can be accessed by all users on a shared computer, realize that the guest virtual machine (VHD) is put in a location that gives Read and Write access to all users on that system.</span></span>

**<span data-ttu-id="54af0-119">도메인 가입에 대 한 프록시 계정 구성</span><span class="sxs-lookup"><span data-stu-id="54af0-119">Configuring a proxy account for domain joining.</span></span>** <span data-ttu-id="54af0-120">도메인에 가상 컴퓨터를 참가 시키는 프록시 계정을 구성 하는 경우 최종 사용자가 프록시 계정 자격 증명을 얻을 수 있는지 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-120">When configuring a proxy account for joining virtual machines to the domain, you must know that it is possible for an end user to obtain the proxy account credentials.</span></span> <span data-ttu-id="54af0-121">따라서 최종 사용자가 해당 자격 증명을 사용 하 여 나쁜 원인이 되는 것을 방지 하기 위해 계정 사용자 권한을 제한 하는 등 필요한 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-121">Thus, necessary precautions must be taken, such as limiting account user rights, to prevent an end user from using the credentials for causing harm.</span></span>

**<span data-ttu-id="54af0-122">Sysprep 구성.</span><span class="sxs-lookup"><span data-stu-id="54af0-122">Sysprep Configuration.</span></span>** <span data-ttu-id="54af0-123">Sysprep.inf 파일은 기본적으로 암호화 되지만, 가상 컴퓨터에 성공적으로 로그온 할 수 있는 결정 된 최종 사용자가 해당 콘텐츠를 해독 하 고 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-123">Although the Sysprep.inf file is encrypted by default, its contents can be decrypted and read by any determined end user who can successfully log on to the virtual machine.</span></span> <span data-ttu-id="54af0-124">이렇게 하면 Sysprep.inf 파일에 Windows 제품 키 외에도 자격 증명이 포함 될 수 있기 때문에 보안 문제를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-124">This raises security concerns because the Sysprep.inf file can contain credentials in addition to a Windows product key.</span></span>

<span data-ttu-id="54af0-125">가상 컴퓨터를 도메인에 가입 하 고 Sysprep을 구성할 때 해당 계정에 대 한 자격 증명을 지정 하는 제한 된 계정을 설정 하 여 이러한 위험을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-125">You can lessen this risk by setting up a limited account for joining virtual machines to the domain and specifying the credentials for that account when configuring Sysprep.</span></span> <span data-ttu-id="54af0-126">또는 Sysprep를 **유인** 모드로 실행 하도록 설정 하 고 최종 사용자가 가상 컴퓨터를 도메인에 연결 하기 위해 자격 증명을 제공 하도록 요구 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-126">Alternately, you can also configure Sysprep and first time setup to run in **Attended** mode and require end users to provide their credentials for joining the virtual machine to the domain.</span></span>

<span data-ttu-id="54af0-127">MED-V 모범 사례는 최종 사용자가 RDC (원격 데스크톱 연결) 클라이언트를 통해 게스트에 연결 하는 데 사용 권한을 부여 하는 계정으로 FtsCompletion.exe를 실행 하도록 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-127">A MED-V best practice is to specify that FtsCompletion.exe is run under an account that gives the end user rights to connect to the guest through the Remote Desktop Connection (RDC) Client.</span></span>

**<span data-ttu-id="54af0-128">최종 사용자 인증.</span><span class="sxs-lookup"><span data-stu-id="54af0-128">End-user authentication.</span></span>** <span data-ttu-id="54af0-129">최종 사용자 자격 증명 캐싱 기능을 사용 하도록 설정 하면 MED-V의 최상의 사용자 환경을 제공 하지만, 최종 사용자의 자격 증명에 대 한 액세스 권한을 얻을 수 있는 가능성도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-129">Enabling the caching of end-user credentials provides the best user experience of MED-V, but creates the potential that someone could gain access to the end user’s credentials.</span></span> <span data-ttu-id="54af0-130">이 위험을 줄이기 위한 유일한 방법은 최종 사용자 자격 증명이 저장 되지 않은 **Med-v 작업 영역 포장기** 를 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="54af0-130">The only way to lessen this risk is by specifying on the **MED-V Workspace Packager** that end-user credentials are not stored.</span></span> <span data-ttu-id="54af0-131">최종 사용자의 인증에 대 한 자세한 내용은 [Med-v 최종 사용자 인증](authentication-of-med-v-end-users.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54af0-131">For more information about authentication of end users, see [Authentication of MED-V End Users](authentication-of-med-v-end-users.md).</span></span>

## <span data-ttu-id="54af0-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="54af0-132">Related topics</span></span>


[<span data-ttu-id="54af0-133">작업 문제 해결</span><span class="sxs-lookup"><span data-stu-id="54af0-133">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

[<span data-ttu-id="54af0-134">Microsoft 엔터프라이즈 데스크톱 가상화 2.0</span><span class="sxs-lookup"><span data-stu-id="54af0-134">Microsoft Enterprise Desktop Virtualization 2.0</span></span>](index.md)

 

 





