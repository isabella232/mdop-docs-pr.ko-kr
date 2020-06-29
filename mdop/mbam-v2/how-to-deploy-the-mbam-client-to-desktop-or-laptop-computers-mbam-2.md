---
title: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
description: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813009"
---
# <span data-ttu-id="93101-103">데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="93101-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="93101-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93101-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="93101-105">Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfigurationManager 같은 전자 소프트웨어 배포 시스템을 통해 클라이언트를 배포 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93101-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="93101-106">**참고**  Microsoft BitLocker 관리 및 클라이언트 시스템 요구 사항 모니터링을 검토 하려면 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93101-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="93101-107">데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="93101-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="93101-108">MBAM 소프트웨어와 함께 제공 되는 MBAM 클라이언트 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="93101-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="93101-109">Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfigurationManager 등의 엔터프라이즈 소프트웨어 배포 도구를 사용 하 여 대상 컴퓨터에 Windows Installer 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="93101-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="93101-110">배포 설정 또는 그룹 정책을 구성 하 여 MBAM 클라이언트 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="93101-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="93101-111">설치가 완료 되 면 MBAM 클라이언트는 도메인 컨트롤러에서 받은 그룹 정책 설정을 적용 하 여 BitLocker 암호화 및 관리 기능을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="93101-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="93101-112">MBAM 그룹 정책 설정에 대 한 자세한 내용은 [mbam 2.0 그룹 정책 요구 사항 계획](planning-for-mbam-20-group-policy-requirements-mbam-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93101-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="93101-113">**중요**  원격 데스크톱 프로토콜 연결이 활성 상태인 경우 MBAM 클라이언트는 BitLocker 암호화 작업을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93101-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="93101-114">BitLocker 암호화를 시작 하기 전에 모든 원격 콘솔 연결을 닫아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93101-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="93101-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="93101-115">Related topics</span></span>


[<span data-ttu-id="93101-116">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="93101-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





