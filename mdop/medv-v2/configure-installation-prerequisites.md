---
title: 설치 필수 구성 요소 구성
description: 설치 필수 구성 요소 구성
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819308"
---
# <span data-ttu-id="6e9e5-103">설치 필수 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="6e9e5-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="6e9e5-104">다음 지침에는 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 설치 및 사용에 대 한 전제 조건이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="6e9e5-105">Windows 가상 PC</span><span class="sxs-lookup"><span data-stu-id="6e9e5-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="6e9e5-106">Windows 가상 PC 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e9e5-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="6e9e5-107">바이러스 백신/백업 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="6e9e5-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="6e9e5-108">Windows 가상 PC를 설치 하 고 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e9e5-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="6e9e5-109">**중요**  Windows 용 Virtual PC 버전이 호스트 컴퓨터에 이미 있는 경우 Windows 가상 PC를 설치 하기 전에 해당 버전을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="6e9e5-110">Windows 가상 PC를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="6e9e5-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="6e9e5-111">Microsoft 다운로드 센터 ()에서 [Windows 가상 PC](https://go.microsoft.com/fwlink/?LinkId=195918) 를 다운로드 https://go.microsoft.com/fwlink/?LinkId=195918) 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="6e9e5-112">호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="6e9e5-113">**중요**  Windows 가상 PC에는 가상 환경과 물리적 컴퓨터 간의 상호 작용을 개선 하는 기능을 제공 하는 통합 구성 요소 패키지가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="6e9e5-114">예를 들어 마우스를 호스트와 게스트 컴퓨터 간에 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="6e9e5-115">MED-V는 통합 구성 요소 패키지를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="6e9e5-116">Windows 가상 PC 업데이트를 설치 하 고 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e9e5-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="6e9e5-117">문서 KB977206에 연결 된 Microsoft 업데이트는 HAV (하드웨어 지원 가상화) 기술이 없는 컴퓨터에 Windows XP 모드를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="6e9e5-118">게스트 운영 체제의 통합 구성 요소 패키지가 호스트 컴퓨터에 설치 된 Windows 가상 PC 버전과 일치 하지 않는 경우 일부 통합 기능이 올바르게 작동 하지 않을 수 있으므로이 업데이트를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="6e9e5-119">**중요**  Windows 7 서비스 팩 1을 실행 하는 호스트 컴퓨터에 MED-V를 설치 하는 경우에는이 업데이트를 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="6e9e5-120">**팁**  여기에 나열 된 업데이트 외에도 사용 가능한 모든 Windows 가상 PC 업데이트를 검토 하 고 해당 환경에 적합 하거나 필요한 업데이트를 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="6e9e5-121">Windows 가상 PC 업데이트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="6e9e5-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="6e9e5-122">Microsoft 다운로드 센터에서 필요한 Windows 가상 PC 업데이트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="6e9e5-123">[32 비트 업데이트](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="6e9e5-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="6e9e5-124">[64 비트 업데이트](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="6e9e5-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="6e9e5-125">관리자 모드의 호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="6e9e5-126">Windows 가상 PC 용 핫픽스 패키지에 대 한 자세한 내용은 [기사 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="6e9e5-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="6e9e5-127">바이러스 백신/백업 소프트웨어를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e9e5-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="6e9e5-128">바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면 호스트 컴퓨터에서 실행 중인 바이러스 백신 또는 백업 프로세스에서 다음 가상 컴퓨터 파일 형식을 제외 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6e9e5-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="6e9e5-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="6e9e5-129">\*.VMC</span></span>

-   <span data-ttu-id="6e9e5-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="6e9e5-130">\*.VUD</span></span>

-   <span data-ttu-id="6e9e5-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="6e9e5-131">\*.VSV</span></span>

-   <span data-ttu-id="6e9e5-132">\*. .VHD</span><span class="sxs-lookup"><span data-stu-id="6e9e5-132">\*.VHD</span></span>

## <span data-ttu-id="6e9e5-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6e9e5-133">Related topics</span></span>


[<span data-ttu-id="6e9e5-134">환경 필수 구성 요소 구성</span><span class="sxs-lookup"><span data-stu-id="6e9e5-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="6e9e5-135">개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="6e9e5-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="6e9e5-136">MED-V 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="6e9e5-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





