---
title: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
description: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824478"
---
# <span data-ttu-id="dfbca-103">데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="dfbca-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="dfbca-104">이 항목에서는 사용자의 컴퓨터에 MBAM 클라이언트를 배포 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="dfbca-105">Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfiguration Manager와 같은 전자 소프트웨어 배포 시스템을 통해 MBAM 클라이언트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="dfbca-106">Windows 배포의 일부로 MBAM 클라이언트를 배포 하려면 [Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker를 사용 하도록 설정 하는 방법을](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfbca-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="dfbca-107">MBAM 클라이언트 배포를 시작 하기 전에 [mbam에서 지원 되는 구성을](mbam-25-supported-configurations.md)검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfbca-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="dfbca-108">데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="dfbca-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="dfbca-109">MBAM 소프트웨어와 함께 제공 되는 MBAM 클라이언트 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="dfbca-110">Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfiguration Manager와 같은 엔터프라이즈 소프트웨어 배포 도구를 사용 하 여 대상 컴퓨터에 Windows Installer 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="dfbca-111">배포 설정 또는 그룹 정책 설정을 구성 하 여 MBAM 클라이언트 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="dfbca-112">설치가 완료 되 면 MBAM 클라이언트는 도메인 컨트롤러에서 받은 그룹 정책 설정을 적용 하 여 BitLocker 드라이브 암호화 및 관리 기능을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="dfbca-113">**중요**  원격 데스크톱 프로토콜 연결이 활성 상태인 경우 MBAM 클라이언트는 BitLocker 드라이브 암호화 작업을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="dfbca-114">모든 원격 콘솔 연결을 종료 해야 하며 사용자는 BitLocker 드라이브 암호화가 시작 되기 전에 물리적 콘솔 세션에 로그온 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="dfbca-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dfbca-115">Related topics</span></span>
[<span data-ttu-id="dfbca-116">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="dfbca-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="dfbca-117">MBAM 2.5 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="dfbca-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="dfbca-118">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="dfbca-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dfbca-119">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="dfbca-120">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbca-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





