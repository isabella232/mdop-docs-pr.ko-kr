---
title: 환경 필수 구성 요소 구성
description: 환경 필수 구성 요소 구성
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826448"
---
# <span data-ttu-id="cb05f-103">환경 필수 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="cb05f-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="cb05f-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0를 배포 하 고 실행 하려면 먼저 환경이 다음 최소 필수 조건을 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="cb05f-105">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb05f-105">Windows 7</span></span>**

<span data-ttu-id="cb05f-106">MED-V 호스트 에이전트 및 MED-V 작업 영역 포장기는 Windows 7 이상 버전 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="cb05f-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="cb05f-107">Windows XP SP3</span></span>**

<span data-ttu-id="cb05f-108">MED-V 게스트 에이전트는 Windows XP SP3 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="cb05f-109">.NET Framework 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="cb05f-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="cb05f-110">MED-V 호스트와 게스트 에이전트 및 MED-V 작업 영역 포장기에는 Microsoft .NET Framework 3.5 SP1이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="cb05f-111">**중요**  또한 [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) https://go.microsoft.com/fwlink/?LinkId=204950) 알려진 여러 응용 프로그램 호환성 문제를 해결 하는 업데이트 KB959209를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="cb05f-112">**참고**  .NET Framework 3.5 SP1 및 업데이트 KB959209을 MED-V와 함께 사용 하기 위해 준비 하는 Windows 가상 PC 이미지에 수동으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="cb05f-113">그러나 호스트 컴퓨터에 Windows 7을 설치 하면 기본적으로 Microsoft .NET Framework 3.5 SP1 및 업데이트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="cb05f-114">Active Directory 인프라</span><span class="sxs-lookup"><span data-stu-id="cb05f-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="cb05f-115">그룹 정책은 Active Directory 환경에서 운영 체제, 응용 프로그램 및 사용자 설정의 중앙 집중화 된 관리 및 구성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb05f-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="cb05f-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cb05f-116">Related topics</span></span>


[<span data-ttu-id="cb05f-117">설치 필수 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="cb05f-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="cb05f-118">개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="cb05f-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="cb05f-119">MED-V 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="cb05f-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





