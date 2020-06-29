---
title: MED-V에 영향을 주는 네트워크 변경 검색
description: MED-V에 영향을 주는 네트워크 변경 검색
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823373"
---
# <span data-ttu-id="d51c8-103">MED-V에 영향을 주는 네트워크 변경 검색</span><span class="sxs-lookup"><span data-stu-id="d51c8-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="d51c8-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 솔루션을 사용 하면 MED-V 작업 영역이 배포 되 고 MED-V에 영향을 줄 수 있는 경우 발생할 수 있는 특정 네트워크 변경을 감지 하도록 환경을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="d51c8-105">이 기능에는 호스트 컴퓨터에서 네트워크 구성 변경 사항에 대 한 알림을 받는 게스트 운영 체제에서 실행 되는 구성 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="d51c8-106">이를 통해 게스트에서 실행 중인 비 Microsoft ESD 또는 다른 응용 프로그램을 사용 하 여 호스트 ESD 또는 응용 프로그램이 확인 하는 동일한 네트워크 끝점을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="d51c8-107">**참고**  이 기능은 가상 컴퓨터가 NAT (network address translation) 모드에 대해 구성 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="d51c8-108">가상 머신이 브리지 모드에 대해 구성 되어 있는 경우 변경 표시가 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="d51c8-109">이 섹션에서는 MED-V에 영향을 줄 수 있는 네트워크 변경을 모니터링 하는 데 도움이 되는 정보와 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="d51c8-110">MED-V에 대 한 네트워크 변경을 감지 하려면</span><span class="sxs-lookup"><span data-stu-id="d51c8-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="d51c8-111">MED-V 작업 영역을 배포한 후에는 다음과 같은 작업을 수행 하 여 특정 네트워크 구성에 대 한 변경 내용을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="d51c8-112">모니터링 하려는 네트워크 구성 변경 내용을 찾을 MOF (관리 개체 형식) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="d51c8-113">다음 코드에서는 만들 수 있는 MOF 파일의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="d51c8-114">MOF 파일을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="d51c8-115">게스트에 MOF 파일을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="d51c8-116">MOF 파일을 설치한 후에는 **CCM \ _NetworkAdapters** 클래스에 대 한 WMI (Windows Management Instrumentation) 만들기, 수정 또는 삭제 이벤트를 구독 하는 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="d51c8-117">이렇게 하면 호스트에 대 한 다음과 같은 변경 내용이 감지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="d51c8-118">IP 주소 또는 네트워크 어댑터 변경 등 네트워크에 대 한 구성 변경 사항이 있나요?</span><span class="sxs-lookup"><span data-stu-id="d51c8-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="d51c8-119">네트워크를 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="d51c8-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="d51c8-120">네트워크 설정이 브리지 모드에서 NAT 모드로 변경 되었습니까?</span><span class="sxs-lookup"><span data-stu-id="d51c8-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="d51c8-121">네트워크 설정이 NAT 모드에서 브리지 모드로 변경 되었습니까?</span><span class="sxs-lookup"><span data-stu-id="d51c8-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="d51c8-122">호스트의 MED-V 구성 요소는 이러한 변경 사항에 대 한 네트워크를 모니터링 하 고 게스트에 게 변경 내용을 알립니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="d51c8-123">게스트의 구성 요소는 이러한 변경 내용에 대 한 MED-V 작업 영역을 모니터링 하는 WMI 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="d51c8-124">생성 된 이벤트 구독은 이러한 네트워크 변경 (만들기, 수정 또는 삭제) 중 하나 이상을 수행 하는 경우 WMI 시스템을 통해 알림을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51c8-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="d51c8-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d51c8-125">Related topics</span></span>


[<span data-ttu-id="d51c8-126">MED-V 작업 영역 모니터링</span><span class="sxs-lookup"><span data-stu-id="d51c8-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="d51c8-127">MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="d51c8-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





