---
title: MBAM 2.0 클라이언트 배포 계획
description: MBAM 2.0 클라이언트 배포 계획
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812620"
---
# <span data-ttu-id="5736f-103">MBAM 2.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="5736f-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="5736f-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 배포 하는 경우 최종 사용자가 컴퓨터를 받거나 나중에 조직의 컴퓨터에서 BitLocker 드라이브 암호화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="5736f-105">MBAM 독립 실행형 및 Configuration Manager 토폴로지에서는 모두 MBAM에 대 한 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="5736f-106">MBAM 독립 실행형 토폴로지를 사용 하는 경우 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 일반 사용자 컴퓨터에 MBAM 클라이언트 소프트웨어를 배포 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="5736f-107">구성 관리자 토폴로지에 MBAM을 배포 하는 경우 구성 관리자를 사용 하 여 MBAM 클라이언트 소프트웨어를 최종 사용자 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="5736f-108">Configuration Manager에서 MBAM 설치는 MBAM이 관리할 수 있는 컴퓨터 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="5736f-109">이 컬렉션에는 TPM (신뢰할 수 있는 플랫폼 모듈)이 없지만 Windows 8을 실행 하는 워크스테이션과 장치가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="5736f-110">**참고**  Windows To Go는 구성 관리자 2007를 사용 하는 경우 MBAM의 통합 된 Configuration Manager 설치에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="5736f-111">컴퓨터 배포 후 최종 사용자에 게 BitLocker 암호화를 사용 하도록 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="5736f-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="5736f-112">그룹 정책을 구성한 후에는 Microsoft System Center Configuration Manager 또는 AD DS (Active Directory 도메인 서비스)와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 MBAM 클라이언트 설치의 Windows Installer 파일을 대상 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="5736f-113">MBAM 클라이언트를 배포 하려면 32 비트 또는 64 비트 MbamClientSetup.exe 파일 또는 MBAM 소프트웨어와 함께 제공 되는 MBAMClient.msi 파일을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="5736f-114">컴퓨터를 클라이언트 컴퓨터에 배포한 후 MBAM 클라이언트를 배포 하는 경우 최종 사용자에 게 컴퓨터를 암호화 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="5736f-115">이를 통해 MBAM이 PIN 및 암호를 포함 하는 데이터를 수집 하 고 암호화 프로세스를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="5736f-116">**참고**  이 방법에서 TPM 칩이 있는 컴퓨터를 사용 하는 사용자는 칩이 이전에 활성화 되지 않은 경우 TPM 칩을 정품 인증 하 고 초기화 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="5736f-117">컴퓨터를 최종 사용자에 게 배포 하기 전에 MBAM 클라이언트를 사용 하 여 BitLocker 암호화를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="5736f-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="5736f-118">컴퓨터가 중앙에서 수신 되 고 구성 되는 조직에서 컴퓨터에 규격 TPM 칩이 있는 경우 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 암호화를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="5736f-119">이 프로세스의 장점은 모든 컴퓨터가 BitLocker 암호화 규격을 준수 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="5736f-120">관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="5736f-121">이 시나리오의 주요 전제는 사용자에 게 컴퓨터를 전달 하기 전에 조직의 정책이 회사 Windows 이미지를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="5736f-122">조직에서 TPM 칩을 사용 하 여 컴퓨터를 암호화 하려는 경우 관리자는 TPM 보호기를 추가 하 여 컴퓨터의 운영 체제 볼륨을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="5736f-123">조직에서 TPM 칩 및 PIN 보호기를 사용 하려는 경우 관리자는 TPM 보호기를 사용 하 여 운영 체제 볼륨을 암호화 한 다음 사용자가 처음으로 로그온 할 때 PIN을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="5736f-124">조직에서 PIN 보호기만 사용 하기로 결정 한 경우 관리자는 먼저 볼륨을 암호화할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="5736f-125">사용자가 로그온 할 때 Microsoft BitLocker 관리 및 모니터링에서 PIN을 제공 하 라는 메시지를 표시 하거나 나중에 컴퓨터를 다시 시작 하는 데 사용할 PIN 및 암호를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="5736f-126">**참고**  TPM 보호기 옵션을 사용 하려면 관리자가 컴퓨터를 사용자에 게 전달 하기 전에 TPM을 활성화 하 고 초기화 하는 BIOS 프롬프트를 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5736f-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="5736f-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5736f-127">Related topics</span></span>


[<span data-ttu-id="5736f-128">MBAM 2.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="5736f-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="5736f-129">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="5736f-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





