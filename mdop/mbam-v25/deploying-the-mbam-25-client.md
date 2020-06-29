---
title: MBAM 2.5 클라이언트 배포
description: MBAM 2.5 클라이언트 배포
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826278"
---
# <span data-ttu-id="0280c-103">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="0280c-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="0280c-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 소프트웨어를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="0280c-105">BitLocker 클라이언트는 Active Directory 도메인 서비스와 같은 전자 소프트웨어 배포 시스템을 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터를 직접 암호화 하 여 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="0280c-106">Microsoft BitLocker 관리 및 모니터링 클라이언트 소프트웨어를 배포 하는 경우 최종 사용자가 컴퓨터를 받은 후 또는 나중에 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MBAM 클라이언트 소프트웨어를 배포 하 고 그룹 정책을 구성 하 여 조직의 컴퓨터에서 BitLocker 드라이브 암호화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="0280c-107">데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="0280c-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="0280c-108">그룹 정책 설정을 구성한 후에는 MicrosoftSystemCenter2012 ConfigurationManager 또는 Active Directory 도메인 서비스와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="0280c-109">32 비트 또는 64 비트 MbamClientSetup.exe 파일을 사용 하거나 MBAM 클라이언트 소프트웨어와 함께 제공 되는 32 비트 또는 64 비트 MBAMClient.msi 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="0280c-110">MBAM 그룹 정책 설정을 배포 하는 방법에 대 한 자세한 내용은 [mbam 2.5 그룹 정책 개체 배포](deploying-mbam-25-group-policy-objects.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0280c-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="0280c-111">**참고**  MBAM 2.5 SP1 부터는 별도의 MSI가 MBAM 제품에 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="0280c-112">그러나 제품에 포함 된 실행 파일 (.exe)에서 MSI를 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="0280c-113">데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="0280c-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="0280c-114">Windows 배포의 일부로 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="0280c-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="0280c-115">컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 드라이브 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="0280c-116">이 프로세스의 장점은 모든 컴퓨터가 BitLocker 드라이브 암호화 규격을 준수 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="0280c-117">관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="0280c-118">이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="0280c-119">PIN을 요구 하도록 그룹 정책 설정을 구성한 경우 사용자가 정책을 받은 후 PIN을 설정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="0280c-120">Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법</span><span class="sxs-lookup"><span data-stu-id="0280c-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="0280c-121">명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="0280c-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="0280c-122">이 섹션에서는 명령줄을 사용 하 여 MBAM 클라이언트를 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="0280c-123">명령줄을 사용하여 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="0280c-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="0280c-124">MBAM 클라이언트 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="0280c-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="0280c-125">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="0280c-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="0280c-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0280c-126">Related topics</span></span>


[<span data-ttu-id="0280c-127">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="0280c-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="0280c-128">MBAM 2.5 계획</span><span class="sxs-lookup"><span data-stu-id="0280c-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="0280c-129">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="0280c-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0280c-130">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0280c-131">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0280c-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





