---
title: MED-V 개요
description: MED-V 개요
author: dansimp
ms.assetid: 393daa9b-2d76-43e1-861a-9d8c00f68cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 047c1d245d286000e7f19078086c00d012f0e10a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825478"
---
# <span data-ttu-id="7672a-103">MED-V 개요</span><span class="sxs-lookup"><span data-stu-id="7672a-103">Overview of MED-V</span></span>


<span data-ttu-id="7672a-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0을 통해 엔터프라이즈 전체에서 Windows 가상 PC 이미지를 배포 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 enables the deployment and management of Windows Virtual PC images throughout an enterprise.</span></span> <span data-ttu-id="7672a-105">Windows 가상 PC를 통해 호스팅되는 Windows XP Professional SP3을 운영 하는 대규모 데스크톱 배포를 제공 하는 경우 MED-V는 일부 응용 프로그램이 아직 제대로 작동 하지 않거나 지원 되지 않는 경우에도 Windows 7로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-105">By providing large-scale deployments of desktops running Windows XP Professional SP3 that are hosted through Windows Virtual PC, MED-V lets businesses upgrade to Windows 7, even though some of their applications might not yet be fully functional or supported.</span></span>

<span data-ttu-id="7672a-106">이 가이드는 MED-V 환경을 이해, 배포 및 관리 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-106">This guide helps you understand, deploy, and manage your MED-V environment.</span></span> <span data-ttu-id="7672a-107">이 가이드에서 제공 하는 정보를 사용 하 여 MED-V 배포를 계획 하 고 준비 하는 방법, med-v 작업 영역을 모니터링 및 관리 하는 방법을 알아보고 MED-V를 사용 하 여 IT 조직에 혜택을 제공 하는 방법을 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-107">By using the information provided in this guide, you can plan for and prepare your MED-V deployment, learn how to monitor and manage MED-V workspaces, and understand how to use MED-V to benefit your IT organization.</span></span>

## <span data-ttu-id="7672a-108">MED-V를 사용하기 위한 주요 시나리오</span><span class="sxs-lookup"><span data-stu-id="7672a-108">Key Scenarios for Using MED-V</span></span>


<span data-ttu-id="7672a-109">새 버전의 Windows와 함께 레거시 응용 프로그램이 호환 되지 않는 경우 엔터프라이즈 업그레이드가 최신 버전의 Windows로 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-109">Incompatibility of legacy applications together with new versions of Windows can often delay enterprise upgrades to the latest version of Windows.</span></span> <span data-ttu-id="7672a-110">응용 프로그램을 테스트 하 고 마이그레이션하는 데 시간이 걸릴 수 있으며, 사용자는 최신 운영 체제에서 제공 하는 새로운 기능과 향상 된 기능을 활용할 수가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-110">Testing and migrating applications takes time, and users cannot take advantage of the new capabilities and enhancements offered by the newest operating system.</span></span>

<span data-ttu-id="7672a-111">Windows XP SP3을 실행 하는 Windows 가상 PC에 응용 프로그램을 제공 하면 MED-V가 운영 체제 업그레이드에 대 한 장애물을 제거 하 고 관리자가 업그레이드 후 호환 되지 않는 응용 프로그램을 테스트 하 고 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-111">By delivering applications in a Windows Virtual PC that is running Windows XP SP3, MED-V removes the barriers to operating system upgrades and lets administrators complete testing and address incompatible applications after the upgrade.</span></span>

<span data-ttu-id="7672a-112">사용자의 관점에서 보면 이러한 응용 프로그램은 표준 바탕 화면 **시작** 메뉴에서 액세스할 수 있으며 기본 응용 프로그램과 나란히 표시 되므로 사용자 환경에 대 한 변경 내용이 최소화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7672a-112">From the user's perspective, these applications can be accessed from the standard desktop **Start** menu and appear side-by-side with native applications, so there is minimal change to the user experience.</span></span>

## <span data-ttu-id="7672a-113">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7672a-113">Related topics</span></span>


[<span data-ttu-id="7672a-114">응용 프로그램 운영 체제 호환성 계획</span><span class="sxs-lookup"><span data-stu-id="7672a-114">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="7672a-115">MED-V 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="7672a-115">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





