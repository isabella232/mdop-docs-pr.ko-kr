---
title: MBAM 2.0용 환경 준비
description: MBAM 2.0용 환경 준비
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825608"
---
# <span data-ttu-id="42eee-103">MBAM 2.0용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="42eee-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="42eee-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="42eee-105">사전 요구 사항이 앞에 있는 것을 알면 제품을 효율적으로 배포 하 고 해당 기능을 사용 하도록 설정 하 여 조직의 비즈니스 목표를 효과적으로 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="42eee-106">Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 배포 하는 경우 [Configuration manager를 사용 하 여 MBAM 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42eee-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="42eee-107">MBAM 2.0 배포 필수 구성 요소 검토</span><span class="sxs-lookup"><span data-stu-id="42eee-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="42eee-108">MBAM 클라이언트와 각 MBAM 서버 기능에는 성공적으로 설치할 수 있으려면 먼저 충족 해야 하는 특정 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="42eee-109">MBAM 클라이언트와 MBAM 서버 기능을 성공적으로 설치 하려면 mbam 클라이언트 또는 MBAM 서버 기능 설치에 대해 지정 된 컴퓨터가 MBAM 설정에 적절 하 게 준비 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="42eee-110">**참고**  MBAM 설치 프로그램이 설치를 시작 하기 전에 모든 필수 구성 요소를 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="42eee-111">모든 선행 조건이 충족 되지 않으면 설치에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="42eee-112">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="42eee-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="42eee-113">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="42eee-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="42eee-114">MBAM이 엔터프라이즈에서 클라이언트를 관리할 수 있으려면 사용자 환경의 암호화 요구 사항에 대 한 그룹 정책을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="42eee-115">**중요**  MBAM은 독립 실행형 BitLocker 드라이브 암호화에 대 한 정책과 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="42eee-116">MBAM에 대해 그룹 정책 설정을 정의 해야 하며, BitLocker 암호화 및 적용이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="42eee-117">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="42eee-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="42eee-118">MBAM 2.0 관리자 역할에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="42eee-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="42eee-119">MBAM 관리자 역할은 BitLocker 관리 및 모니터링 서버, 준수 및 감사 보고서 기능, 준수 및 감사 상태 데이터베이스를 설치할 때 MBAM 설정으로 만든 로컬 그룹에서 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="42eee-120">Microsoft BitLocker 관리 및 모니터링 역할의 구성원은 ActiveDirectoryDomainServices에서 보안 그룹을 만들고 해당 그룹에 적절 한 관리자 계정을 추가한 다음 해당 보안 그룹을 BitLocker 관리 및 로컬 그룹 모니터링에 추가 하 여 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42eee-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="42eee-121">자세한 내용은 [MBAM 관리자 역할을 관리 하는 방법을](how-to-manage-mbam-administrator-roles-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42eee-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="42eee-122">MBAM 계획에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="42eee-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="42eee-123">MBAM 2.0 계획</span><span class="sxs-lookup"><span data-stu-id="42eee-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="42eee-124">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="42eee-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





