---
title: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
description: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825543"
---
# <span data-ttu-id="917d9-103">데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="917d9-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="917d9-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="917d9-105">MBAM 클라이언트는 Active Directory 도메인 서비스 또는 MicrosoftSystemCenter2012 ConfigurationManager 등의 엔터프라이즈 소프트웨어 배포 도구를 통해 클라이언트를 배포 하 여 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="917d9-106">**참고**  MBAM 클라이언트 시스템 요구 사항을 검토 하려면 [mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="917d9-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="917d9-107">데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="917d9-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="917d9-108">MBAM 소프트웨어와 함께 제공 되는 MBAM 클라이언트 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="917d9-109">Active Directory 도메인 서비스 또는 엔터프라이즈 소프트웨어 배포 도구 (예: MicrosoftSystemCenter2012 ConfigurationManager)를 사용 하 여 대상 컴퓨터에 Windows Installer 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="917d9-110">**참고**  Windows Installer 패키지를 배포 하는 데 그룹 정책을 사용 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="917d9-111">배포 설정 또는 그룹 정책을 구성 하 여 MBAM 클라이언트 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="917d9-112">설치가 완료 되 면 MBAM 클라이언트는 도메인 컨트롤러에서 받은 그룹 정책 설정을 적용 하 여 BitLocker 암호화 및 관리 기능을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="917d9-113">MBAM 그룹 정책 설정에 대 한 자세한 내용은 [mbam 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="917d9-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="917d9-114">**중요**  원격 데스크톱 프로토콜 연결이 활성 상태인 경우 MBAM 클라이언트는 BitLocker 암호화 작업을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="917d9-115">BitLocker 암호화를 시작 하기 전에 모든 원격 콘솔 연결을 닫아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="917d9-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="917d9-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="917d9-116">Related topics</span></span>


[<span data-ttu-id="917d9-117">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="917d9-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





