---
title: MBAM 2.5용 환경 준비
description: MBAM 2.5용 환경 준비
author: dansimp
ms.assetid: 7552ba08-9dbf-40cd-8920-203d733fd242
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b18c9853035018c2e36dd447fbf0effbf49c45cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825493"
---
# <span data-ttu-id="0ab7b-103">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="0ab7b-103">Preparing your Environment for MBAM 2.5</span></span>


<span data-ttu-id="0ab7b-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 설정을 시작 하기 전에 제품을 설치 하기 위한 전제 조건을 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="0ab7b-105">사전 요구 사항이 앞에 있는 것을 알면 제품을 효율적으로 배포 하 고 해당 기능을 사용 하도록 설정 하 여 조직의 비즈니스 목표를 효과적으로 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="0ab7b-106">Configuration Manager를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 배포 하는 경우이 항목의 뒷부분에 나열 된 구성 관리자에 대 한 추가 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Configuration Manager, ensure that you meet the additional requirements for Configuration Manager, which are listed later in this topic.</span></span>

## <span data-ttu-id="0ab7b-107">MBAM 2.5 배포 필수 구성 요소 검토</span><span class="sxs-lookup"><span data-stu-id="0ab7b-107">Review MBAM 2.5 deployment prerequisites</span></span>


<span data-ttu-id="0ab7b-108">MBAM 배포가 성공적으로 수행 되도록 하려면 MBAM 클라이언트를 설치 하 고 MBAM 서버 기능을 구성 하기 전에 필수 소프트웨어 필수 구성 요소를 검토 하 고 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-108">To ensure that your MBAM deployment is successful, make sure that you review and complete the required software prerequisites before you install the MBAM Client and configure the MBAM Server features.</span></span>

[<span data-ttu-id="0ab7b-109">MBAM 2.5 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="0ab7b-109">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)

## <span data-ttu-id="0ab7b-110">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="0ab7b-110">Plan for MBAM 2.5 Group Policy requirements</span></span>


<span data-ttu-id="0ab7b-111">MBAM이 엔터프라이즈에서 클라이언트를 관리할 수 있으려면 먼저 MBAM에 해당 하는 그룹 정책 템플릿을 다운로드 하 고 구성한 다음 환경에 맞게 원하는 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-111">Before MBAM can manage clients in the enterprise, you must download and configure Group Policy templates that are specific to MBAM, and then configure the Group Policy settings that you want for your environment.</span></span>

[<span data-ttu-id="0ab7b-112">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="0ab7b-112">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

## <span data-ttu-id="0ab7b-113">MBAM 2.5 역할 및 계정에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="0ab7b-113">Plan for MBAM 2.5 roles and accounts</span></span>


<span data-ttu-id="0ab7b-114">필수 구성 요소의 일환으로 특정 역할 및 계정 (예: MBAM에서 보안 및 액세스 권한을 제공 하는 데 사용 되며, SQL Server에서 실행 되는 데이터베이스와 관리 및 모니터링 서버에서 실행 되는 웹 응용 프로그램)</span><span class="sxs-lookup"><span data-stu-id="0ab7b-114">As part of the prerequisites, you must define certain roles and accounts, which are used in MBAM to provide security and access rights to specific servers and features, such as the databases running on SQL Server and the web applications running on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="0ab7b-115">MBAM 2.5 그룹 및 계정 계획</span><span class="sxs-lookup"><span data-stu-id="0ab7b-115">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)

## <span data-ttu-id="0ab7b-116">MBAM 계획에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="0ab7b-116">Other resources for MBAM planning</span></span>


[<span data-ttu-id="0ab7b-117">MBAM 2.5 계획</span><span class="sxs-lookup"><span data-stu-id="0ab7b-117">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="0ab7b-118">MBAM 2.5 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="0ab7b-118">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="0ab7b-119">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="0ab7b-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0ab7b-120">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0ab7b-121">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab7b-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





