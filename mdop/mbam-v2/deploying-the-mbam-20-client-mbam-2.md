---
title: MBAM 2.0 클라이언트 배포
description: MBAM 2.0 클라이언트 배포
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823448"
---
# <span data-ttu-id="c8997-103">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="c8997-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="c8997-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="c8997-105">BitLocker 클라이언트는 Active Directory 도메인 서비스와 같은 전자 소프트웨어 배포 시스템을 통해 클라이언트를 배포 하거나 초기 이미지 프로세스의 일부로 클라이언트 컴퓨터를 직접 암호화 하 여 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="c8997-106">Microsoft BitLocker 관리 및 모니터링 클라이언트를 배포 하는 경우 최종 사용자가 컴퓨터를 받기 전에 또는 나중에 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MBAM 클라이언트 소프트웨어를 배포 하 고 그룹 정책을 구성 하 여 조직의 컴퓨터에서 BitLocker 암호화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="c8997-107">데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="c8997-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="c8997-108">그룹 정책을 구성한 후 Microsoft System Center Configuration Manager 2012 또는 Active Directory 도메인 서비스와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="c8997-109">32 비트 또는 64 비트 MbamClientSetup.exe 파일 또는 MBAM 소프트웨어와 함께 제공 되는 32 비트 또는 64 비트 MBAMClient.msi 파일을 사용 하 여 클라이언트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="c8997-110">MBAM 그룹 정책 개체를 배포 하는 방법에 대 한 자세한 내용은 [mbam 2.0 그룹 정책 개체 배포](deploying-mbam-20-group-policy-objects-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8997-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="c8997-111">데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="c8997-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="c8997-112">Windows 배포의 일부로 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="c8997-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="c8997-113">컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="c8997-114">이 프로세스의 장점은 모든 컴퓨터가 BitLocker 암호화 규격을 준수 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="c8997-115">관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="c8997-116">이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="c8997-117">그룹 정책이 PIN을 요구 하도록 구성 된 경우 사용자가 그룹 정책을 받은 후 PIN을 설정 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="c8997-118">Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="c8997-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="c8997-119">명령줄을 사용하여 MBAM 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="c8997-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="c8997-120">이 섹션에서는 명령줄을 사용 하 여 MBAM 클라이언트를 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8997-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="c8997-121">명령줄을 사용하여 MBAM 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="c8997-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="c8997-122">MBAM 클라이언트 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="c8997-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="c8997-123">Mbam [2.0](deploying-mbam-20-mbam-2.md)[2.0 계획 배포 클라이언트 배포](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="c8997-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





