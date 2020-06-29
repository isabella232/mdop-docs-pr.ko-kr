---
title: MBAM 1.0 클라이언트 배포 계획
description: MBAM 1.0 클라이언트 배포 계획
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825878"
---
# <span data-ttu-id="cb870-103">MBAM 1.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="cb870-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="cb870-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 배포 하는 경우 최종 사용자가 컴퓨터를 받거나 나중에 조직의 컴퓨터에서 BitLocker 암호화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="cb870-105">최종 사용자가 컴퓨터를 받은 후 BitLocker 암호화를 사용 하도록 설정 하려면 그룹 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="cb870-106">최종 사용자가 컴퓨터를 받기 전에 BitLocker 암호화를 사용 하도록 설정 하려면 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MBAM 클라이언트 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="cb870-107">조직에서 하나 또는 두 가지 방법 모두를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="cb870-108">두 방법을 모두 사용 하는 경우 준수, 보고 및 키 복구 지원을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="cb870-109">**참고**  MBAM 클라이언트 시스템 요구 사항을 검토 하려면 [mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb870-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="cb870-110">컴퓨터 배포 후 최종 사용자에 게 BitLocker 암호화를 사용 하도록 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="cb870-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="cb870-111">그룹 정책을 구성한 후에는 Microsoft System Center Configuration Manager 2012 또는 Active Directory 도메인 서비스와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 MBAM 클라이언트 설치 Windows Installer 파일을 대상 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="cb870-112">두 개의 MBAM 클라이언트 설치 Windows Installer 파일은 MBAMClient-64bit.msi 및 MBAMClient-32bit.msi 이며이는 MBAM 소프트웨어와 함께 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="cb870-113">MBAM 그룹 정책 개체를 배포 하는 방법에 대 한 자세한 내용은 [mbam 1.0 그룹 정책 개체 배포](deploying-mbam-10-group-policy-objects.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb870-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="cb870-114">MBAM 클라이언트를 배포 하는 경우 컴퓨터를 최종 사용자에 게 배포 하면 최종 사용자에 게 컴퓨터를 암호화 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="cb870-115">이렇게 하면 MBAM이 데이터를 수집 하 고, PIN 및 암호를 포함 하 고, 암호화 프로세스를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="cb870-116">**참고**  이 방법에서는 TPM (신뢰할 수 있는 플랫폼 모듈) 칩이 이전에 활성화 되지 않은 경우이를 활성화 하 고 초기화 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="cb870-117">컴퓨터를 최종 사용자에 게 배포 하기 전에 MBAM 클라이언트를 사용 하 여 BitLocker 암호화를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="cb870-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="cb870-118">컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="cb870-119">이 프로세스의 장점은 모든 컴퓨터가 BitLocker 암호화를 준수 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="cb870-120">관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="cb870-121">이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="cb870-122">조직에서 컴퓨터를 암호화 하기 위해 (TPM)을 사용 하려는 경우 관리자는 TPM 보호기를 사용 하 여 컴퓨터의 운영 체제 볼륨을 암호화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="cb870-123">조직에서 TPM 칩 및 PIN 보호기를 사용 하려는 경우 관리자는 TPM 보호기를 사용 하 여 시스템 볼륨을 암호화 한 다음 사용자가 처음 로그온 할 때 PIN을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="cb870-124">조직에서 PIN 보호기만 사용 하기로 결정 한 경우 관리자는 먼저 볼륨을 암호화할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="cb870-125">사용자가 컴퓨터에 로그온 할 때 MBAM은 PIN 또는 PIN을 입력 하 라는 메시지를 표시 하 고 나중에 컴퓨터를 다시 시작할 때 사용할 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="cb870-126">**참고**  TPM 보호기 옵션은 컴퓨터를 사용자에 게 전달 하기 전에 관리자가 BIOS 프롬프트를 수락 하 여 TPM을 정품 인증 하 고 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb870-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="cb870-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cb870-127">Related topics</span></span>


[<span data-ttu-id="cb870-128">MBAM 1.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="cb870-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="cb870-129">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="cb870-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





